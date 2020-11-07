---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: c1d7a7128c0fd4774c99799695e0d041a08c8053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664780"
---
# <span data-ttu-id="3e096-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="3e096-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="3e096-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e096-102">SYNOPSIS</span></span>
<span data-ttu-id="3e096-103">Ruft die Eigenschaften eines Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="3e096-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e096-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e096-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e096-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e096-105">DESCRIPTION</span></span>
<span data-ttu-id="3e096-106">Das Cmdlet " **Get-AzureRmImage** " Ruft die Eigenschaften eines Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="3e096-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="3e096-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e096-107">EXAMPLES</span></span>

### <span data-ttu-id="3e096-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e096-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="3e096-109">Dieser Befehl ruft die Eigenschaften des Bilds mit dem Namen "Image01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="3e096-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3e096-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3e096-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="3e096-111">Dieser Befehl ruft die Eigenschaften aller Bilder in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="3e096-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3e096-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3e096-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="3e096-113">Mit diesem Befehl werden die Eigenschaften aller Bilder unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3e096-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="3e096-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e096-114">PARAMETERS</span></span>

### <span data-ttu-id="3e096-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e096-115">-DefaultProfile</span></span>
<span data-ttu-id="3e096-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e096-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e096-117">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="3e096-117">-Expand</span></span>
<span data-ttu-id="3e096-118">Gibt die Expand-Ausdrucks Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="3e096-118">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e096-119">-Bildname</span><span class="sxs-lookup"><span data-stu-id="3e096-119">-ImageName</span></span>
<span data-ttu-id="3e096-120">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="3e096-120">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e096-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e096-121">-ResourceGroupName</span></span>
<span data-ttu-id="3e096-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3e096-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e096-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e096-123">CommonParameters</span></span>
<span data-ttu-id="3e096-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e096-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e096-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e096-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e096-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e096-126">INPUTS</span></span>

### <span data-ttu-id="3e096-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3e096-127">System.String</span></span>

## <span data-ttu-id="3e096-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e096-128">OUTPUTS</span></span>

### <span data-ttu-id="3e096-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="3e096-129">System.Object</span></span>

## <span data-ttu-id="3e096-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e096-130">NOTES</span></span>

## <span data-ttu-id="3e096-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e096-131">RELATED LINKS</span></span>

