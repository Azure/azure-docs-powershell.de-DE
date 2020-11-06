---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497729"
---
# <span data-ttu-id="96505-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="96505-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="96505-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96505-102">SYNOPSIS</span></span>
<span data-ttu-id="96505-103">Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="96505-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96505-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96505-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="96505-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96505-105">DESCRIPTION</span></span>
<span data-ttu-id="96505-106">Das Cmdlet " **Get-AzureRmSnapshot** " Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="96505-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="96505-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96505-107">EXAMPLES</span></span>

### <span data-ttu-id="96505-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="96505-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="96505-109">Dieser Befehl ruft die Eigenschaften aller Snapshots des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="96505-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="96505-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="96505-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="96505-111">Dieser Befehl ruft die Eigenschaften aller Schnappschüsse in der Ressourcengruppe mit dem Namen "ResourceGroupName1" ab.</span><span class="sxs-lookup"><span data-stu-id="96505-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="96505-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="96505-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="96505-113">Mit diesem Befehl werden die Eigenschaften des Snapshots mit dem Namen "SnapshotName1" in der Ressourcengruppe "ResourceGroupName1" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="96505-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="96505-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="96505-114">PARAMETERS</span></span>

### <span data-ttu-id="96505-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96505-115">-ResourceGroupName</span></span>
<span data-ttu-id="96505-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="96505-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96505-117">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="96505-117">-SnapshotName</span></span>
<span data-ttu-id="96505-118">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="96505-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96505-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96505-119">CommonParameters</span></span>
<span data-ttu-id="96505-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96505-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96505-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96505-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96505-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96505-122">INPUTS</span></span>

### <span data-ttu-id="96505-123">System. String</span><span class="sxs-lookup"><span data-stu-id="96505-123">System.String</span></span>

## <span data-ttu-id="96505-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96505-124">OUTPUTS</span></span>

### <span data-ttu-id="96505-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="96505-125">System.Object</span></span>

## <span data-ttu-id="96505-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="96505-126">NOTES</span></span>

## <span data-ttu-id="96505-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96505-127">RELATED LINKS</span></span>

