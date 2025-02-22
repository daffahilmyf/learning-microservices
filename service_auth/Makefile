# Define directories where proto files are generated
PROTO_DIRS := $(shell find . -type d -name "proto")

# Find all generated proto files
PROTO_GEN_FILES := $(shell find . -type f -name "*.pb.go")

# Clean generated proto files
.PHONY: clean-proto
clean-proto:
	@echo "Removing generated protobuf files..."
	@rm -f $(PROTO_GEN_FILES)
	@echo "Done!"

# Generate protobuf files using buf
.PHONY: gen-proto
gen-proto:
	@echo "Generating protobuf files using buf..."
	@buf generate
	@echo "Done!"