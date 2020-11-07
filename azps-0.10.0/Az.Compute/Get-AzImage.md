---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 13829081952be7ab79c6d7badde4dc687aa845ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844644"
---
# <span data-ttu-id="045c4-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="045c4-101">Get-AzImage</span></span>

## <span data-ttu-id="045c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="045c4-102">SYNOPSIS</span></span>
<span data-ttu-id="045c4-103">Ruft die Eigenschaften eines Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="045c4-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="045c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="045c4-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="045c4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="045c4-105">DESCRIPTION</span></span>
<span data-ttu-id="045c4-106">Das Cmdlet " **Get-AzImage** " Ruft die Eigenschaften eines Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="045c4-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="045c4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="045c4-107">EXAMPLES</span></span>

### <span data-ttu-id="045c4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="045c4-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="045c4-109">Dieser Befehl ruft die Eigenschaften des Bilds mit dem Namen "Image01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="045c4-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="045c4-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="045c4-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="045c4-111">Dieser Befehl ruft die Eigenschaften aller Bilder in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="045c4-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="045c4-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="045c4-112">Example 3</span></span>
```
PS C:\> Get-AzImage
```

<span data-ttu-id="045c4-113">Mit diesem Befehl werden die Eigenschaften aller Bilder unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="045c4-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="045c4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="045c4-114">PARAMETERS</span></span>

### <span data-ttu-id="045c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="045c4-115">-DefaultProfile</span></span>
<span data-ttu-id="045c4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="045c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="045c4-117">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="045c4-117">-Expand</span></span>
<span data-ttu-id="045c4-118">Gibt die Expand-Ausdrucks Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="045c4-118">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="045c4-119">-Bildname</span><span class="sxs-lookup"><span data-stu-id="045c4-119">-ImageName</span></span>
<span data-ttu-id="045c4-120">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="045c4-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="045c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="045c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="045c4-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="045c4-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="045c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045c4-123">CommonParameters</span></span>
<span data-ttu-id="045c4-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="045c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045c4-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="045c4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045c4-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="045c4-126">INPUTS</span></span>

### <span data-ttu-id="045c4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="045c4-127">System.String</span></span>

## <span data-ttu-id="045c4-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="045c4-128">OUTPUTS</span></span>

### <span data-ttu-id="045c4-129">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="045c4-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="045c4-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="045c4-130">NOTES</span></span>

## <span data-ttu-id="045c4-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="045c4-131">RELATED LINKS</span></span>

