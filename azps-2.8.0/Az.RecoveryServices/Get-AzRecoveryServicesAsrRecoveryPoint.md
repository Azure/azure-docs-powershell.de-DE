---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: b381f611d47306c9327d1b276aa3773c34c7b3e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824384"
---
# <span data-ttu-id="9a24a-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9a24a-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="9a24a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a24a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a24a-103">Ruft die verfügbaren Wiederherstellungspunkte für ein geschütztes Replikations Element ab.</span><span class="sxs-lookup"><span data-stu-id="9a24a-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="9a24a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a24a-104">SYNTAX</span></span>

### <span data-ttu-id="9a24a-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a24a-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a24a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9a24a-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a24a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a24a-107">DESCRIPTION</span></span>
<span data-ttu-id="9a24a-108">Das Cmdlet " **Get-AzRecoveryServicesAsrRecoveryPoint** " Ruft die Liste der verfügbaren Wiederherstellungspunkte für ein geschütztes Replikations Element ab.</span><span class="sxs-lookup"><span data-stu-id="9a24a-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="9a24a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a24a-109">EXAMPLES</span></span>

### <span data-ttu-id="9a24a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a24a-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="9a24a-111">Ruft Wiederherstellungspunkte für das angegebene ASR-Replikations geschützte Element ab.</span><span class="sxs-lookup"><span data-stu-id="9a24a-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="9a24a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a24a-112">PARAMETERS</span></span>

### <span data-ttu-id="9a24a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a24a-113">-DefaultProfile</span></span>
<span data-ttu-id="9a24a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a24a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9a24a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9a24a-115">-Name</span></span>
<span data-ttu-id="9a24a-116">Gibt den Namen des abzurufenden Wiederherstellungspunkts an.</span><span class="sxs-lookup"><span data-stu-id="9a24a-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a24a-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a24a-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9a24a-118">Gibt das Azure Site Recovery Replication Protected Item-Objekt an, für das die Liste der verfügbaren Wiederherstellungspunkte abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a24a-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="9a24a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a24a-119">CommonParameters</span></span>
<span data-ttu-id="9a24a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a24a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a24a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a24a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a24a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a24a-122">INPUTS</span></span>

### <span data-ttu-id="9a24a-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9a24a-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="9a24a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a24a-124">OUTPUTS</span></span>

### <span data-ttu-id="9a24a-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9a24a-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="9a24a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a24a-126">NOTES</span></span>

## <span data-ttu-id="9a24a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a24a-127">RELATED LINKS</span></span>

[<span data-ttu-id="9a24a-128">Bearbeiten-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9a24a-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9a24a-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9a24a-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9a24a-130">Neu – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9a24a-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9a24a-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9a24a-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9a24a-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9a24a-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
