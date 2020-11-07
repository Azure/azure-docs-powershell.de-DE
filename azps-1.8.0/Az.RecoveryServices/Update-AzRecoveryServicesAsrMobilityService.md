---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 6dd1c87617d83754af430ae25aea1b47aaaa34e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659787"
---
# <span data-ttu-id="95126-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="95126-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="95126-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95126-102">SYNOPSIS</span></span>
<span data-ttu-id="95126-103">Push-Updates für Mobilitätsdienst-Agents auf geschützten Computern</span><span class="sxs-lookup"><span data-stu-id="95126-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="95126-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95126-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95126-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95126-105">DESCRIPTION</span></span>
<span data-ttu-id="95126-106">Das Cmdlet **Update-AzRecoveryServicesAsrMobilityService** versucht, Mobilitätsdienst-Agent-Updates auf geschützte Computer zu übertragen (sofern ein Update verfügbar ist).</span><span class="sxs-lookup"><span data-stu-id="95126-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="95126-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95126-107">EXAMPLES</span></span>

### <span data-ttu-id="95126-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95126-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="95126-109">Job zum Nachvollziehen des Moblility-Service-Agents für das Update-Replikations Element</span><span class="sxs-lookup"><span data-stu-id="95126-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="95126-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95126-110">PARAMETERS</span></span>

### <span data-ttu-id="95126-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="95126-111">-Account</span></span>
<span data-ttu-id="95126-112">Die ID des ausführbaren Kontos, die zum Pushen des Updates verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95126-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="95126-113">Muss eine aus der Liste der ausführende Konten im ASR-Fabric sein, die der zu aktualisierende Maschine entspricht.</span><span class="sxs-lookup"><span data-stu-id="95126-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95126-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95126-114">-DefaultProfile</span></span>
<span data-ttu-id="95126-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95126-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95126-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95126-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="95126-117">Geschütztes Element der Azure Site Recovery-Replikation, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="95126-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95126-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95126-118">-Confirm</span></span>
<span data-ttu-id="95126-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95126-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95126-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95126-120">-WhatIf</span></span>
<span data-ttu-id="95126-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95126-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95126-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95126-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95126-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95126-123">CommonParameters</span></span>
<span data-ttu-id="95126-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95126-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95126-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95126-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95126-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95126-126">INPUTS</span></span>

### <span data-ttu-id="95126-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="95126-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="95126-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95126-128">OUTPUTS</span></span>

### <span data-ttu-id="95126-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="95126-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="95126-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="95126-130">NOTES</span></span>

## <span data-ttu-id="95126-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95126-131">RELATED LINKS</span></span>
