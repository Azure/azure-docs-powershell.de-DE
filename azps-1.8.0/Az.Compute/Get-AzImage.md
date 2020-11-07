---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: ffebc22d2ad5c28c40d79ffb9c6ba8b5ba5bf5a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661565"
---
# <span data-ttu-id="dd167-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="dd167-101">Get-AzImage</span></span>

## <span data-ttu-id="dd167-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd167-102">SYNOPSIS</span></span>
<span data-ttu-id="dd167-103">Ruft die Eigenschaften eines Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="dd167-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="dd167-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd167-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd167-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd167-105">DESCRIPTION</span></span>
<span data-ttu-id="dd167-106">Das Cmdlet " **Get-AzImage** " Ruft die Eigenschaften eines Bilds ab.</span><span class="sxs-lookup"><span data-stu-id="dd167-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="dd167-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd167-107">EXAMPLES</span></span>

### <span data-ttu-id="dd167-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd167-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="dd167-109">Dieser Befehl ruft die Eigenschaften des Bilds mit dem Namen "Image01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="dd167-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="dd167-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dd167-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="dd167-111">Dieser Befehl ruft die Eigenschaften aller Bilder in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="dd167-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="dd167-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="dd167-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="dd167-113">Mit diesem Befehl werden die Eigenschaften aller Bilder unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dd167-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="dd167-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="dd167-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="dd167-115">Dieser Befehl ruft die Eigenschaften aller Bilder unter dem Abonnement ab, die mit "Image" beginnen.</span><span class="sxs-lookup"><span data-stu-id="dd167-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="dd167-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd167-116">PARAMETERS</span></span>

### <span data-ttu-id="dd167-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd167-117">-DefaultProfile</span></span>
<span data-ttu-id="dd167-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd167-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd167-119">– Erweitern</span><span class="sxs-lookup"><span data-stu-id="dd167-119">-Expand</span></span>
<span data-ttu-id="dd167-120">Gibt die Expand-Ausdrucks Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="dd167-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd167-121">-Bildname</span><span class="sxs-lookup"><span data-stu-id="dd167-121">-ImageName</span></span>
<span data-ttu-id="dd167-122">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="dd167-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd167-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd167-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd167-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dd167-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dd167-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd167-125">CommonParameters</span></span>
<span data-ttu-id="dd167-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd167-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd167-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd167-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd167-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd167-128">INPUTS</span></span>

### <span data-ttu-id="dd167-129">System. String</span><span class="sxs-lookup"><span data-stu-id="dd167-129">System.String</span></span>

## <span data-ttu-id="dd167-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd167-130">OUTPUTS</span></span>

### <span data-ttu-id="dd167-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="dd167-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="dd167-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd167-132">NOTES</span></span>

## <span data-ttu-id="dd167-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd167-133">RELATED LINKS</span></span>
