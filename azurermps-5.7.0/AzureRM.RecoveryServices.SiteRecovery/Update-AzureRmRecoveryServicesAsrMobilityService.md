---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: de9e07da334e252db4af87819d2719b5251b576c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476649"
---
# <span data-ttu-id="ffc59-101">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="ffc59-101">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="ffc59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffc59-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc59-103">Push-Updates für Mobilitätsdienst-Agents auf geschützten Computern</span><span class="sxs-lookup"><span data-stu-id="ffc59-103">Push mobility service agent updates to protected machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffc59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffc59-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc59-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffc59-105">DESCRIPTION</span></span>
<span data-ttu-id="ffc59-106">Das Cmdlet **Update-AzureRmRecoveryServicesAsrMobilityService** versucht, Mobilitätsdienst-Agent-Updates auf geschützte Computer zu übertragen (sofern ein Update verfügbar ist).</span><span class="sxs-lookup"><span data-stu-id="ffc59-106">The **Update-AzureRmRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="ffc59-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffc59-107">EXAMPLES</span></span>

### <span data-ttu-id="ffc59-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ffc59-108">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="ffc59-109">Job zum Nachvollziehen des Moblility-Service-Agents für das Update-Replikations Element</span><span class="sxs-lookup"><span data-stu-id="ffc59-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="ffc59-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffc59-110">PARAMETERS</span></span>

### <span data-ttu-id="ffc59-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="ffc59-111">-Account</span></span>
<span data-ttu-id="ffc59-112">Die ID des ausführbaren Kontos, die zum Pushen des Updates verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffc59-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="ffc59-113">Muss eine aus der Liste der ausführende Konten im ASR-Fabric sein, die der zu aktualisierende Maschine entspricht.</span><span class="sxs-lookup"><span data-stu-id="ffc59-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc59-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffc59-114">-Confirm</span></span>
<span data-ttu-id="ffc59-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffc59-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc59-116">-DefaultProfile</span></span>
<span data-ttu-id="ffc59-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffc59-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffc59-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ffc59-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ffc59-119">Geschütztes Element der Azure Site Recovery-Replikation, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffc59-119">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc59-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc59-120">-WhatIf</span></span>
<span data-ttu-id="ffc59-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffc59-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffc59-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffc59-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc59-123">CommonParameters</span></span>
<span data-ttu-id="ffc59-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc59-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc59-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc59-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffc59-126">INPUTS</span></span>

### <span data-ttu-id="ffc59-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ffc59-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ffc59-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffc59-128">OUTPUTS</span></span>

### <span data-ttu-id="ffc59-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ffc59-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ffc59-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffc59-130">NOTES</span></span>

## <span data-ttu-id="ffc59-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffc59-131">RELATED LINKS</span></span>
