SET(ATen_CUDA_SRCS ${ATen_CUDA_SRCS}
${CMAKE_CURRENT_SOURCE_DIR}/BCECriterion.cu
${CMAKE_CURRENT_SOURCE_DIR}/ClassNLLCriterion.cu
${CMAKE_CURRENT_SOURCE_DIR}/ELU.cu
${CMAKE_CURRENT_SOURCE_DIR}/GatedLinearUnit.cu
${CMAKE_CURRENT_SOURCE_DIR}/HardTanh.cu
${CMAKE_CURRENT_SOURCE_DIR}/LeakyReLU.cu
${CMAKE_CURRENT_SOURCE_DIR}/LogSigmoid.cu
${CMAKE_CURRENT_SOURCE_DIR}/MultiLabelMarginCriterion.cu
${CMAKE_CURRENT_SOURCE_DIR}/MultiMarginCriterion.cu
${CMAKE_CURRENT_SOURCE_DIR}/RReLU.cu
${CMAKE_CURRENT_SOURCE_DIR}/SoftMarginCriterion.cu
${CMAKE_CURRENT_SOURCE_DIR}/SoftPlus.cu
${CMAKE_CURRENT_SOURCE_DIR}/SoftShrink.cu
${CMAKE_CURRENT_SOURCE_DIR}/SpatialClassNLLCriterion.cu
${CMAKE_CURRENT_SOURCE_DIR}/SpatialConvolutionMM.cu
${CMAKE_CURRENT_SOURCE_DIR}/SpatialDepthwiseConvolution.cu
${CMAKE_CURRENT_SOURCE_DIR}/Tanh.cu
PARENT_SCOPE)

set(ATen_CUDA_INCLUDE ${ATen_CUDA_INCLUDE}
  "${CMAKE_CURRENT_SOURCE_DIR}"
PARENT_SCOPE)

install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
  DESTINATION ${ATEN_INSTALL_INCLUDE_SUBDIR}
  FILES_MATCHING PATTERN "*.h" PATTERN "*.cuh")
