# Superpixel Segmentation using Depth Information / Code

The code provided as part of the bachelor thesis "Superpixel Segmentation using Depth Information" [1]:

* Revised implementation of the SEEDS superpixel algorithm [2]: [SEEDS Revised](https://github.com/davidstutz/seeds-revised).
* Superpixel library containing several of the evaluated algorithms: [Superpixels Revisited](https://github.com/davidstutz/superpixels-revisited).
* Benchmark used for evaluation of all superpixel algorithms: [Extended Berkeley Segmentation Benchmark](https://github.com/davidstutz/extended-berkeley-segmentation-benchmark).
* Tool for working with the NYU Depth Dataset V2 [3]: [NYU Depth V2 Tools](https://github.com/davidstutz/nyu-depth-v2-tools).
* Interactive plots of comparison based on [nvd3](http://nvd3.org/): [nvd3 Superpixel Comparison](https://github.com/davidstutz/nvd3-superpixel-comparison).

# Usage

Evaluation on the [Berkeley Segmentation Dataset (BSDS500)](http://www.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/resources.html) [4] or on the [NYU Depth Dataset V2 (NYUV2)](http://cs.nyu.edu/~silberman/datasets/nyu_depth_v2.html) [3]:

1. Download the BSDS500 or the NYUV2.
    * The NYUV2 dataset was split into training and test set according to `nyu-depth-v2-tools/list_train.txt` and `nyu-depth-v2-tools/list_test.txt`, respectively. Then subsets were selected according to `nyu-depth-v2-tools/list_train_subset.txt` and `nyu-depth-v2-tools/list_test_subset.txt` (using `nyu-depth-v2-tools/convert_dataset.m`, `nyu-depth-v2-tools/collect_train_subset.m` and `nyu-depth-v2-tools/collect_test_subset.m`). All images were cropped using `nyu-depth-v2-tools/crop_dataset.m`.
    * The BSDS500 already provides training and test set.
3. Compile all superpixel algorithms using the instructions in `superpixels-revisited/README.md`.
4. Set up the extended version of the Berkeley Segmentation Benchmark [5] according to `extended-berkeley-segmentation-benchmark/README.md`.

All command line tools in `superpixels-revisited` provide a `--csv` option in order to save all generated superpixel segmentations in the form of CSV files (also use `--output my_output_folder/`). The extended Berkeley Segmentation Benchmark provides [`extended-berkeley-segmentation-benchmark/convert_csv_bsd.m`](https://github.com/davidstutz/extended-berkeley-segmentation-benchmark/blob/master/benchmarks/convert_csv_bsd.m) used to convert CSV files to the BSDS500 groundtruth format. For further instructions on using the extended Berkeley Segmentation Benchmark, see [`extended-berkeley-segmentation-benchmark/README.md`](https://github.com/davidstutz/extended-berkeley-segmentation-benchmark).

## File Index

* [SEEDS Revised](https://github.com/davidstutz/seeds-revised)
* [Superpixels Revisited](https://github.com/davidstutz/superpixels-revisited)
* [Extended Berkeley Segmentation Benchmark](https://github.com/davidstutz/extended-berkeley-segmentation-benchmark)
* [NYU Depth V2 Tools](https://github.com/davidstutz/nyu-depth-v2-tools)
* [nvd3 Superpixel Comparison](https://github.com/davidstutz/nvd3-superpixel-comparison)

## References

    [1] D. Stutz, A. Hermans, B. Leibe.
        Superpixel Segmentation using Depth Information.
        Bachelor thesis, RWTH Aachen University, Aachen, Germany, 2014.
    [2] M. van den Bergh, X. Boix, G. Roig, B. de Capitani, L. van Gool.
        SEEDS: Superpixels extracted via energy-driven sampling.
        European Conference on Computer Vision, pages 13–26, 2012.
    [3] N. Silberman, D. Hoiem, P. Kohli, R. Fergus.
        Indoor segmentation and support inference from RGBD images.
        In Computer Vision, European Conference on, volume 7576 of Lecture Notes in Computer Science, pages 746–760. Springer Berlin Heidelberg, 2012.
    [4] P. Arbeláez, M. Maire, C. Fowlkes, J. Malik. 
        Contour detection and hierarchical image segmentation.
        Transactions on Pattern Analysis and Machine Intelligence, 33(5):898–916, 2011
    [5] P. Arbeláez, M. Maire, C. Fowlkes, J. Malik.
        Contour detection and hierarchical image segmentation.
        Transactions on Pattern Analysis and Machine Intelligence, volume 33, number 5, pages 898–916, 2011.

## License

See the corresponding subrepositories for license information.
