---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermimage
schema: 2.0.0
ms.openlocfilehash: 8508a7353924342449324588e90abf3807d7f7ac
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849404"
---
# <span data-ttu-id="b3ca8-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="b3ca8-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="b3ca8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ca8-103">Ruft die Eigenschaften eines Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ca8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3ca8-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3ca8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3ca8-105">DESCRIPTION</span></span>
<span data-ttu-id="b3ca8-106">Das Cmdlet " **Get-AzureRmImage** " Ruft die Eigenschaften eines Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="b3ca8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3ca8-107">EXAMPLES</span></span>

### <span data-ttu-id="b3ca8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3ca8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="b3ca8-109">Dieser Befehl ruft die Eigenschaften des Bilds mit dem Namen "Image01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b3ca8-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b3ca8-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="b3ca8-111">Dieser Befehl ruft die Eigenschaften aller Bilder in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b3ca8-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b3ca8-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="b3ca8-113">Mit diesem Befehl werden die Eigenschaften aller Bilder unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="b3ca8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3ca8-114">PARAMETERS</span></span>

### <span data-ttu-id="b3ca8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ca8-115">-DefaultProfile</span></span>
<span data-ttu-id="b3ca8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3ca8-117">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="b3ca8-117">-Expand</span></span>
<span data-ttu-id="b3ca8-118">Gibt die Expand-Ausdrucks Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-118">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ca8-119">-Bildname</span><span class="sxs-lookup"><span data-stu-id="b3ca8-119">-ImageName</span></span>
<span data-ttu-id="b3ca8-120">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b3ca8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ca8-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3ca8-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b3ca8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ca8-123">CommonParameters</span></span>
<span data-ttu-id="b3ca8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3ca8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ca8-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ca8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ca8-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3ca8-126">INPUTS</span></span>

### <span data-ttu-id="b3ca8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b3ca8-127">System.String</span></span>

## <span data-ttu-id="b3ca8-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3ca8-128">OUTPUTS</span></span>

### <span data-ttu-id="b3ca8-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b3ca8-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b3ca8-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3ca8-130">NOTES</span></span>

## <span data-ttu-id="b3ca8-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3ca8-131">RELATED LINKS</span></span>

