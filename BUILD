load(
  "@fpga_rules//vivado:rules.bzl",
  "fpga_bitstream"
)
load(
  "@fpga_rules//clash:rules.bzl",
  "clash_to_verilog"
)


fpga_bitstream(
  name = "blinkenlights",
  srcs = [
    ":blinkenlights_clash"
  ],
  part = "xc7z020clg400-1",
  constraints = [
    "const.xdc"
  ],
  topEntity = "topEntity",
  optimize = False
)

clash_to_verilog(
  name = "blinkenlights_clash",
  srcs = [
    "BlinkenLights.hs"
  ],
  outputs = [
    "verilog/BlinkenLights/topEntity.v"
  ],
  top_entity = "BlinkenLights.hs"
)
