---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: e344dd4b5284a29c84b4f4c4b90d5a99f5d8d4ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824415"
---
# <span data-ttu-id="4494d-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="4494d-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="4494d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4494d-102">SYNOPSIS</span></span>
<span data-ttu-id="4494d-103">Ruft Informationen zu den Netzwerken ab, die von der Websitewiederherstellung für den aktuellen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4494d-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="4494d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4494d-104">SYNTAX</span></span>

### <span data-ttu-id="4494d-105">ByFabricObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="4494d-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4494d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4494d-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4494d-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4494d-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4494d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4494d-108">DESCRIPTION</span></span>
<span data-ttu-id="4494d-109">Das Cmdlet " **Get-AzRecoveryServicesAsrNetwork** " Ruft Informationen zu Azure Site Recovery Networks für das aktuelle Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="4494d-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="4494d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4494d-110">EXAMPLES</span></span>

### <span data-ttu-id="4494d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4494d-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="4494d-112">Ruft alle bekannten Netzwerke im angegebenen Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="4494d-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="4494d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4494d-113">PARAMETERS</span></span>

### <span data-ttu-id="4494d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4494d-114">-DefaultProfile</span></span>
<span data-ttu-id="4494d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4494d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4494d-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="4494d-116">-Fabric</span></span>
<span data-ttu-id="4494d-117">ASR-Fabric-Objekt</span><span class="sxs-lookup"><span data-stu-id="4494d-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4494d-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4494d-118">-FriendlyName</span></span>
<span data-ttu-id="4494d-119">Anzeigename des Network ASR-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4494d-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4494d-120">-Name</span></span>
<span data-ttu-id="4494d-121">Name des Network ASR-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4494d-121">Name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4494d-122">CommonParameters</span></span>
<span data-ttu-id="4494d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4494d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4494d-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4494d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4494d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4494d-125">INPUTS</span></span>

### <span data-ttu-id="4494d-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4494d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4494d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4494d-127">OUTPUTS</span></span>

### <span data-ttu-id="4494d-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="4494d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="4494d-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4494d-129">NOTES</span></span>

## <span data-ttu-id="4494d-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4494d-130">RELATED LINKS</span></span>
