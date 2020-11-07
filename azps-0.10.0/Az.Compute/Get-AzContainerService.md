---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844664"
---
# <span data-ttu-id="d9373-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d9373-101">Get-AzContainerService</span></span>

## <span data-ttu-id="d9373-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9373-102">SYNOPSIS</span></span>
<span data-ttu-id="d9373-103">Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="d9373-103">Gets a container service.</span></span>

## <span data-ttu-id="d9373-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9373-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9373-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9373-105">DESCRIPTION</span></span>
<span data-ttu-id="d9373-106">Das Cmdlet " **Get-AzContainerService** " Ruft einen Containerdienst ab.</span><span class="sxs-lookup"><span data-stu-id="d9373-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="d9373-107">Sie können die Eigenschaften eines Container Diensts anzeigen, der den Status, die Anzahl der Master und Agents sowie den vollqualifizierten Domänennamenmaster und Agent umfasst.</span><span class="sxs-lookup"><span data-stu-id="d9373-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="d9373-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9373-108">EXAMPLES</span></span>

### <span data-ttu-id="d9373-109">Beispiel 1: Abrufen eines Container Diensts</span><span class="sxs-lookup"><span data-stu-id="d9373-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="d9373-110">Dieser Befehl ruft einen Containerdienst mit dem Namen CSResourceGroup17 ab.</span><span class="sxs-lookup"><span data-stu-id="d9373-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="d9373-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9373-111">PARAMETERS</span></span>

### <span data-ttu-id="d9373-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9373-112">-DefaultProfile</span></span>
<span data-ttu-id="d9373-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9373-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9373-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d9373-114">-Name</span></span>
<span data-ttu-id="d9373-115">Gibt den Namen des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d9373-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9373-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9373-116">-ResourceGroupName</span></span>
<span data-ttu-id="d9373-117">Gibt die Ressourcengruppe des Container Diensts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d9373-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9373-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9373-118">CommonParameters</span></span>
<span data-ttu-id="d9373-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9373-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9373-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9373-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9373-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9373-121">INPUTS</span></span>

### <span data-ttu-id="d9373-122">Keine</span><span class="sxs-lookup"><span data-stu-id="d9373-122">None</span></span>
<span data-ttu-id="d9373-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d9373-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9373-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9373-124">OUTPUTS</span></span>

### <span data-ttu-id="d9373-125">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d9373-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d9373-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9373-126">NOTES</span></span>

## <span data-ttu-id="d9373-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9373-127">RELATED LINKS</span></span>

[<span data-ttu-id="d9373-128">Neu – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d9373-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="d9373-129">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d9373-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="d9373-130">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d9373-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


