# Build the libWireCellLarsoft WCT plugin library.
# See README for some details.

# This is what's needed for building the WireCellLarsoft WCT component
# plugin library.
cet_make_library(LIBRARY_NAME WireCellLarsoft
  SOURCE
  ChannelNoiseDB.cxx
  ChannelSelectorDB.cxx
  CookedFrameSink.cxx
  CookedFrameSource.cxx
  DepoSetSimChannelSink.cxx
  FrameSaver.cxx
  LazyFrameSource.cxx
  MultiChannelNoiseDB.cxx
  RawFrameSource.cxx
  SimChannelSink.cxx
  SimDepoSetSource.cxx
  SimDepoSource.cxx
  LIBRARIES
  PUBLIC
  larwirecell::IArtEventVisitor
  larcoreobj::headers
  canvas::canvas
  WireCell::SigProc
  WireCell::Iface
  WireCell::Util
  lardataobj::Simulation
  PRIVATE
  larevt::CalibrationDBI_IOVData
  larevt::ChannelStatusService
  larevt::ChannelStatusProvider
  larevt::DetPedestalService
  larevt::DetPedestalProvider
  larevt::ElectronicsCalibService
  larevt::ElectronicsCalibProvider
  lardata::DetectorPropertiesService
  larcore::Geometry_Geometry_service
  larcore::ServiceUtil
  lardataobj::RecoBase
  lardataobj::RawData
  art::Framework_Core
  art::Framework_Principal
  WireCell::Gen
  ROOT::Core
)
