---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportService.md
ms.openlocfilehash: 019f37fa6b735b506c71a914a6ea59700565fd49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846168"
---
# <span data-ttu-id="23006-101">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="23006-101">Get-AzSupportService</span></span>

## <span data-ttu-id="23006-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23006-102">SYNOPSIS</span></span>
<span data-ttu-id="23006-103">Abrufen von Diensten, für die Support verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="23006-103">Get services for which support is available.</span></span> 

## <span data-ttu-id="23006-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23006-104">SYNTAX</span></span>

### <span data-ttu-id="23006-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="23006-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportService [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23006-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23006-106">GetByNameParameterSet</span></span>
```
Get-AzSupportService -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23006-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23006-107">DESCRIPTION</span></span>
<span data-ttu-id="23006-108">Ruft die aktuelle Liste der Azure-Dienste ab, für die Unterstützung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="23006-108">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="23006-109">Jeder Dienst kann einen oder mehrere Ressourcentyp Informationen des Azure Resource Manager (Arm) enthalten.</span><span class="sxs-lookup"><span data-stu-id="23006-109">Each service may contain one or more Azure resource manager (ARM) resource type information.</span></span> <span data-ttu-id="23006-110">Ressourcentypen (Beispiel: "Microsoft. Compute/VirtualMachines") können nützlich sein, wenn Sie beim Erstellen eines Technical Support-Tickets das richtige Produkt und die richtige Arm-Ressource zuordnen.</span><span class="sxs-lookup"><span data-stu-id="23006-110">Resource types (example: 'microsoft.compute/virtualmachines') can be useful to map the right product and ARM resource when creating a technical support ticket.</span></span> <span data-ttu-id="23006-111">Jeder Azure-Dienst verfügt über einen eigenen Satz von Kategorien, die so genannte Problem Klassifikation.</span><span class="sxs-lookup"><span data-stu-id="23006-111">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="23006-112">Rufen Sie die aktuelle Liste der Problemklassifizierung für einen Dienst mithilfe von Get-AzSupportProblemClassification ab.</span><span class="sxs-lookup"><span data-stu-id="23006-112">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="23006-113">Sie können die GUID des Diensts und der Problemklassifizierung verwenden, um ein neues Support Ticket mithilfe von New-AzSupportTicket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="23006-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="23006-114">Verwenden Sie immer die GUIDs des Diensts und der Problemklassifizierung, die programmgesteuert abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="23006-114">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="23006-115">Diese Vorgehensweise stellt sicher, dass Sie über die neuesten GUIDs für Dienst-und Problem Klassifikationen für die Erstellung von Support Tickets verfügen.</span><span class="sxs-lookup"><span data-stu-id="23006-115">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="23006-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23006-116">EXAMPLES</span></span>

### <span data-ttu-id="23006-117">Beispiel 1: Abrufen aller verfügbaren Dienste für Support</span><span class="sxs-lookup"><span data-stu-id="23006-117">Example 1: Get all services available for support</span></span>
```powershell
PS C:\> Get-AzSupportService

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
809e8afe-489e-08b0-95f2-08f835a383e8 Advanced Threat Protection - Azure
6859f4e8-4a1d-13e4-f276-6d055007e83d Advanced Threat Protection - Microsoft Defender
94332e54-73b0-b8e3-306e-db3ad13d950b Advanced Threat Protection - O365
26d8424b-0a41-4443-cbc6-0309ea8708d0 Advisor
8f1ddc5f-0c5e-50c7-9810-e01a8d1da925 AKS Engine on Azure Stack
c1840ac9-309f-f235-c0ae-4782f283b698 Alerts and Action Groups
e8fe7c6f-d883-c57f-6576-cf801ca30653 Analysis Services
07651e65-958a-0877-36f3-61bbba85d783 API for FHIR
b4d0e877-0166-0474-9a76-b5be30ba40e4 API Management Service
e14f616b-42c5-4515-3d7c-67935eece51a App Configuration
445c0905-55e2-4f42-d853-ec9e17a5180e App Service Certificates
b7d2f8b7-7d20-cf2f-ddd5-5543ada54bd2 App Service Domains
101732bb-31af-ee61-7c16-d4ad77c86a50 Application Gateway
```

### <span data-ttu-id="23006-118">Beispiel 2: Abrufen von Details zu einem einzelnen Dienst nach ID, der zur Unterstützung zur Verfügung steht</span><span class="sxs-lookup"><span data-stu-id="23006-118">Example 2: Get details of a single service by id available for support</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "484e2236-bc6d-b1bb-76d2-7d09278cf9ea"

Name                                 DisplayName
----                                 -----------
484e2236-bc6d-b1bb-76d2-7d09278cf9ea Activity Logs
```

## <span data-ttu-id="23006-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="23006-119">PARAMETERS</span></span>

### <span data-ttu-id="23006-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23006-120">-DefaultProfile</span></span>
<span data-ttu-id="23006-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23006-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23006-122">-ID</span><span class="sxs-lookup"><span data-stu-id="23006-122">-Id</span></span>
<span data-ttu-id="23006-123">Dienst-ID.</span><span class="sxs-lookup"><span data-stu-id="23006-123">Service id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23006-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23006-124">CommonParameters</span></span>
<span data-ttu-id="23006-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23006-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23006-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23006-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23006-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23006-127">INPUTS</span></span>

### <span data-ttu-id="23006-128">Keine</span><span class="sxs-lookup"><span data-stu-id="23006-128">None</span></span>

## <span data-ttu-id="23006-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23006-129">OUTPUTS</span></span>

### <span data-ttu-id="23006-130">Microsoft. Azure. Commands. Support. Models. PSSupportService</span><span class="sxs-lookup"><span data-stu-id="23006-130">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="23006-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="23006-131">NOTES</span></span>

## <span data-ttu-id="23006-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23006-132">RELATED LINKS</span></span>
