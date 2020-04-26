load(
  "@fpga_rules//vivado:rules.bzl",
  "fpga_bitstream"
)
load(
  "@fpga_rules//clash:rules.bzl",
  "clash_to_vhdl"
)


fpga_bitstream(
  name = "blinkenlights",
  srcs = [
    "vhdl/BlinkenLights/topentity.vhdl",
    "vhdl/BlinkenLights/blinkenlights_types.vhdl"
  ],
  part = "xc7z020clg400-1",
  constraints = [
    "const.xdc"
  ],
  topEntity = "topEntity",
  optimize = False
)

clash_to_vhdl(
  name = "blinkenlights_clash",
  srcs = [
    "BlinkenLights.hs"
  ],
  outputs = [
    "vhdl/BlinkenLights/blinkenlights_types.vhdl",
    "vhdl/BlinkenLights/topentity.vhdl",
  ],
  top_entity = "BlinkenLights.hs"
)
