---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165712"
---
# <span data-ttu-id="843f0-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="843f0-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="843f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="843f0-102">SYNOPSIS</span></span>
<span data-ttu-id="843f0-103">Ruft Informationen zu den Netzwerkzuordnungen der Websitewiederherstellung für den aktuellen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="843f0-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="843f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="843f0-104">SYNTAX</span></span>

### <span data-ttu-id="843f0-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="843f0-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="843f0-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="843f0-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="843f0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="843f0-107">DESCRIPTION</span></span>
<span data-ttu-id="843f0-108">Das Cmdlet " **Get-AzRecoveryServicesAsrNetworkMapping** " Ruft Informationen zu Azure Site Recovery Network-Zuordnungen für den Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="843f0-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="843f0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="843f0-109">EXAMPLES</span></span>

### <span data-ttu-id="843f0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="843f0-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="843f0-111">Ruft alle Netz Zuordnungen für das übergebene Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="843f0-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="843f0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="843f0-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="843f0-113">Ruft die Netzwerkzuordnung mit dem bereitgestellten Namen in der angegebenen Azure Site Recovery-Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="843f0-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="843f0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="843f0-114">PARAMETERS</span></span>

### <span data-ttu-id="843f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="843f0-115">-DefaultProfile</span></span>
<span data-ttu-id="843f0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="843f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="843f0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="843f0-117">-Name</span></span>
<span data-ttu-id="843f0-118">Der Name des abzurufenden ASR-Netzwerk Zuordnungsobjekts.</span><span class="sxs-lookup"><span data-stu-id="843f0-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="843f0-119">-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="843f0-119">-Network</span></span>
<span data-ttu-id="843f0-120">Rufen Sie die ASR-Netzwerkzuordnungen ab, die dem angegebenen Netzwerk ASR-Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="843f0-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="843f0-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="843f0-121">-PrimaryFabric</span></span>
<span data-ttu-id="843f0-122">Rufen Sie die ASR-Netzwerkzuordnungen ab, die dem angegebenen primären Fabric-Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="843f0-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="843f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="843f0-123">CommonParameters</span></span>
<span data-ttu-id="843f0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="843f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="843f0-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="843f0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="843f0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="843f0-126">INPUTS</span></span>

### <span data-ttu-id="843f0-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="843f0-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="843f0-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="843f0-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="843f0-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="843f0-129">OUTPUTS</span></span>

### <span data-ttu-id="843f0-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="843f0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="843f0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="843f0-131">NOTES</span></span>

## <span data-ttu-id="843f0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="843f0-132">RELATED LINKS</span></span>

[<span data-ttu-id="843f0-133">Neu – AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="843f0-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="843f0-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="843f0-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
