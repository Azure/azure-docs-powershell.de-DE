---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303388"
---
# <span data-ttu-id="eae45-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="eae45-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="eae45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eae45-102">SYNOPSIS</span></span>
<span data-ttu-id="eae45-103">Fügen Sie den Datenträger zum Schutz für bereits geschützten Azure Virtual Machine hinzu.</span><span class="sxs-lookup"><span data-stu-id="eae45-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="eae45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eae45-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eae45-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eae45-105">DESCRIPTION</span></span>
<span data-ttu-id="eae45-106">Das **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk-** Cmdlet fügt den Datenträger zum Schutz für bereits geschützten Azure Virtual Machine hinzu.</span><span class="sxs-lookup"><span data-stu-id="eae45-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="eae45-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eae45-107">EXAMPLES</span></span>

### <span data-ttu-id="eae45-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eae45-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="eae45-109">Starten Sie den Vorgang, um die angegebene Datenträgerkonfiguration für den Schutz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="eae45-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="eae45-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="eae45-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="eae45-111">Starten Sie den Vorgang, um die angegebene Datenträgerkonfiguration für den Schutz hinzuzufügen. Geschütztes Element für die Rohrleitungs Eingabe Replikation</span><span class="sxs-lookup"><span data-stu-id="eae45-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="eae45-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eae45-112">PARAMETERS</span></span>

### <span data-ttu-id="eae45-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="eae45-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="eae45-114">Gibt die Datenträgerkonfiguration an, die für den Datenträgerschutz für Azure to Azure Disaster Recovery-Szenario verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eae45-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eae45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae45-115">-DefaultProfile</span></span>
<span data-ttu-id="eae45-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eae45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eae45-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eae45-117">-InputObject</span></span>
<span data-ttu-id="eae45-118">Das Eingabeobjekt für das Cmdlet: das Objekt der ASR-Replikation, das dem neuen Datenträger entspricht, der geschützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="eae45-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eae45-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="eae45-119">-WaitForCompletion</span></span>
<span data-ttu-id="eae45-120">Auf Abschluss warten</span><span class="sxs-lookup"><span data-stu-id="eae45-120">Wait For Completion</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eae45-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eae45-121">-Confirm</span></span>
<span data-ttu-id="eae45-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eae45-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eae45-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eae45-123">-WhatIf</span></span>
<span data-ttu-id="eae45-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eae45-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eae45-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eae45-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eae45-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae45-126">CommonParameters</span></span>
<span data-ttu-id="eae45-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eae45-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae45-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eae45-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae45-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eae45-129">INPUTS</span></span>

### <span data-ttu-id="eae45-130">Keine</span><span class="sxs-lookup"><span data-stu-id="eae45-130">None</span></span>

## <span data-ttu-id="eae45-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eae45-131">OUTPUTS</span></span>

### <span data-ttu-id="eae45-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eae45-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eae45-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="eae45-133">NOTES</span></span>

## <span data-ttu-id="eae45-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eae45-134">RELATED LINKS</span></span>
