# AVS
Uber Autonomous Visualization System (AVS)

https://user-images.githubusercontent.com/42335542/125196097-12e10380-e28b-11eb-93d2-2d230de11b9b.mp4


## To run example of AVS
```
$ sudo apt install nodejs npm
$ sudo npm install --global yarn
```

## Clone XVIZ
```
$ git clone https://github.com/uber/xviz.git
$ cd xviz
```

## Download Datashet
- Download [synced+rectified data](https://s3.eu-central-1.amazonaws.com/avg-kitti/raw_data/2011_09_26_drive_0005/2011_09_26_drive_0005_sync.zip)
- Download [tracklets](https://s3.eu-central-1.amazonaws.com/avg-kitti/raw_data/2011_09_26_drive_0005/2011_09_26_drive_0005_tracklets.zip)
- Unzip, combine the folder and move the data into xviz

```
/data/kitti
    |- 2011_09_26
        |- 2011_09_26_drive_0005_sync
            |- tracklet_labels.xml
            |- image_00
            |- image_01
            |- image_02
            |- image_03
            |- oxts
            |- velodyne_points
```

## Install dependencies
```
$ sudo python3 -m pip install pykitti
$ cd xviz
$ yarn bootstrap
```

## Convert and serve KITTI example data
```
$ ./scripts/run-kitti-example.sh
```

## Run example client
```
$ git clone https://github.com/uber/streetscape.gl.git
$ cd streetscape.gl
$ yarn bootstrap
$ cd examples/get-started
$ yarn start-streaming local
```

## References
1. https://avs.auto/#/xviz/getting-started/converting-to-xviz/downloading-data
