---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497741"
---
# <span data-ttu-id="37a5b-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="37a5b-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="37a5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="37a5b-103">Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="37a5b-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37a5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37a5b-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="37a5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="37a5b-106">Das Cmdlet " **Get-AzureRmContainerService** " Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="37a5b-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="37a5b-107">Sie können die Eigenschaften eines Container Diensts anzeigen, der den Status, die Anzahl der Master und Agents sowie den vollqualifizierten Domänennamenmaster und Agent umfasst.</span><span class="sxs-lookup"><span data-stu-id="37a5b-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="37a5b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37a5b-108">EXAMPLES</span></span>

### <span data-ttu-id="37a5b-109">Beispiel 1: Abrufen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="37a5b-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="37a5b-110">Dieser Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 ab.</span><span class="sxs-lookup"><span data-stu-id="37a5b-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="37a5b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="37a5b-111">PARAMETERS</span></span>

### <span data-ttu-id="37a5b-112">-Name</span><span class="sxs-lookup"><span data-stu-id="37a5b-112">-Name</span></span>
<span data-ttu-id="37a5b-113">Gibt den Namen des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="37a5b-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37a5b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a5b-114">-ResourceGroupName</span></span>
<span data-ttu-id="37a5b-115">Gibt die Ressourcengruppe des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="37a5b-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="37a5b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a5b-116">CommonParameters</span></span>
<span data-ttu-id="37a5b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a5b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a5b-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a5b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a5b-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37a5b-119">INPUTS</span></span>

### <span data-ttu-id="37a5b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="37a5b-120">None</span></span>
<span data-ttu-id="37a5b-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="37a5b-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37a5b-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37a5b-122">OUTPUTS</span></span>

## <span data-ttu-id="37a5b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="37a5b-123">NOTES</span></span>

## <span data-ttu-id="37a5b-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37a5b-124">RELATED LINKS</span></span>

[<span data-ttu-id="37a5b-125">Neu – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="37a5b-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="37a5b-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="37a5b-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="37a5b-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="37a5b-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


