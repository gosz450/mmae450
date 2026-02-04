
# ===============================
# Makefile for MMAE 450 (Beamer)
# ===============================

LATEX      = pdflatex
LATEXFLAGS = -interaction=nonstopmode

BUILD_DIR  = build
LECTURE_DIR= lectures

LECTURES = \
lecture01_course_introduction \
lecture02_taylor_series_1D \
lecture03_nonlinear_systems_2D \
lecture04_newtons_method_nonlinear_sytems \
lecture05_divergence_theorem \
lecture06_1D_heat_conduction_ftcs \
lecture07_1D_heat_conduction_ftcs_bcs \
lecture08_1D_heat_conduction_cn \
lecture09_2D_heat_conduction \
lecture10_2D_indexing \
lecture11_stability_von_neumann \
lecture12_wave_equation_1D \

PDFS = $(addprefix $(BUILD_DIR)/, $(addsuffix .pdf, $(LECTURES)))

.PHONY: all lectures clean distclean sync help

# Default target
all: lectures

# Build all lecture PDFs
lectures: $(PDFS)

$(BUILD_DIR)/%.pdf: $(LECTURE_DIR)/%.tex | $(BUILD_DIR)
	$(LATEX) $(LATEXFLAGS) -output-directory=$(BUILD_DIR) $<
	$(LATEX) $(LATEXFLAGS) -output-directory=$(BUILD_DIR) $<

# Ensure build directory exists
$(BUILD_DIR):
	mkdir -p $(BUILD_DIR)

# Clean PDFs only
clean:
	@echo "==> Cleaning PDFs in $(BUILD_DIR)"
	@rm -f $(BUILD_DIR)/*.pdf

# Remove entire build directory
distclean: clean
	@echo "==> Removing $(BUILD_DIR) directory"
	@rm -rf $(BUILD_DIR)

# Optional: copy selected PDFs into modules/*/slides
# Adjust mappings as needed as the course evolves
sync: lectures
	@echo "==> Syncing PDFs into modules/*/slides"
	@cp -f $(BUILD_DIR)/lecture01_course_introduction.pdf        ../modules/module01_foundations/slides/lecture01.pdf
	@cp -f $(BUILD_DIR)/lecture02_taylor_series_1D.pdf           ../modules/module01_foundations/slides/lecture02.pdf
	@cp -f $(BUILD_DIR)/lecture03_nonlinear_systems_2D.pdf       ../modules/module02_newtons_method_nonlinear_systems/slides/lecture03.pdf
	@cp -f $(BUILD_DIR)/lecture04_newtons_method_nonlinear_sytems.pdf ../modules/module02_newtons_method_nonlinear_systems/slides/lecture04.pdf
	@cp -f $(BUILD_DIR)/lecture05_divergence_theorem.pdf         ../modules/module03_1D_heat_conduction/slides/lecture05.pdf
	@cp -f $(BUILD_DIR)/lecture06_1D_heat_conduction_ftcs.pdf    ../modules/module03_1D_heat_conduction/slides/lecture06.pdf
	@cp -f $(BUILD_DIR)/lecture07_1D_heat_conduction_ftcs_bcs.pdf    ../modules/module03_1D_heat_conduction/slides/lecture07.pdf
	@cp -f $(BUILD_DIR)/lecture08_1D_heat_conduction_cn.pdf    ../modules/module03_1D_heat_conduction/slides/lecture08.pdf
	@cp -f $(BUILD_DIR)/lecture09_2D_heat_conduction.pdf    ../modules/module04_2D_heat_conduction_wave_propagation/slides/lecture09.pdf
	@cp -f $(BUILD_DIR)/lecture10_2D_indexing.pdf    ../modules/module04_2D_heat_conduction_wave_propagation/slides/lecture10.pdf
	@cp -f $(BUILD_DIR)/lecture11_stability_von_neumann.pdf    ../modules/module04_2D_heat_conduction_wave_propagation/slides/lecture11.pdf
	@cp -f $(BUILD_DIR)/lecture12_wave_equation_1D.pdf    ../modules/module04_2D_heat_conduction_wave_propagation/slides/lecture12.pdf
	@echo "==> Done."

# Help
help:
	@echo "Targets:"
	@echo "  make            Build all lecture PDFs into tex/build/"
	@echo "  make sync       Build and copy PDFs into modules/*/slides"
	@echo "  make clean      Remove PDFs in tex/build/"
	@echo "  make distclean  Remove tex/build/ entirely"
