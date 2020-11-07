---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 8133bfc8381f08e69afbd6bfbd3a25084e9eb2b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848911"
---
# <span data-ttu-id="b8d8b-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b8d8b-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="b8d8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d8b-103">Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8d8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8d8b-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8d8b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d8b-106">Das Cmdlet " **Get-AzureRmSnapshot** " Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="b8d8b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="b8d8b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8d8b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="b8d8b-109">Dieser Befehl ruft die Eigenschaften aller Snapshots des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="b8d8b-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b8d8b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="b8d8b-111">Dieser Befehl ruft die Eigenschaften aller Schnappschüsse in der Ressourcengruppe mit dem Namen "ResourceGroupName1" ab.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="b8d8b-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b8d8b-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="b8d8b-113">Mit diesem Befehl werden die Eigenschaften des Snapshots mit dem Namen "SnapshotName1" in der Ressourcengruppe "ResourceGroupName1" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="b8d8b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8d8b-114">PARAMETERS</span></span>

### <span data-ttu-id="b8d8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d8b-115">-DefaultProfile</span></span>
<span data-ttu-id="b8d8b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d8b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d8b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b8d8b-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b8d8b-119">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="b8d8b-119">-SnapshotName</span></span>
<span data-ttu-id="b8d8b-120">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b8d8b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d8b-121">CommonParameters</span></span>
<span data-ttu-id="b8d8b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d8b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d8b-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d8b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d8b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8d8b-124">INPUTS</span></span>

### <span data-ttu-id="b8d8b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b8d8b-125">System.String</span></span>

## <span data-ttu-id="b8d8b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8d8b-126">OUTPUTS</span></span>

### <span data-ttu-id="b8d8b-127">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b8d8b-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b8d8b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8d8b-128">NOTES</span></span>

## <span data-ttu-id="b8d8b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8d8b-129">RELATED LINKS</span></span>

