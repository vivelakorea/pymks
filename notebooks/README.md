# notes

- plot_microstructures

```
plot_microstructures(
    2-d array 1,
    2-d array 2,
    2-d array 3, ...,
    titles=['array1', 'array2', 'array3', ...],
    cmap='...'
    )
```

- PrimitiveTransformer
  이미지 데이터를 min\_, max\_ 설정에 따라

- how to make transformer

```
model = Pipeline(step=[
    ('discretize', PrimitiveTransformer(n_state=2, min_=0.0, max_=1.0)),
    ('correlations', TwoPointCorrelation(
        periodic_boundary=True,
        cutoff=x_data.shape[1],
        correlations=[[0, 0], [0, 1], [1, 1]]
    ))
])
```
