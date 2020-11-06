---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478922"
---
# <span data-ttu-id="1ccdc-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ccdc-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="1ccdc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ccdc-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccdc-103">Ermöglicht die Replikation für ein geschütztes Element durch Erstellen eines geschützten Elements.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ccdc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ccdc-104">SYNTAX</span></span>

### <span data-ttu-id="1ccdc-105">Disabled (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ccdc-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ccdc-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="1ccdc-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ccdc-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1ccdc-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ccdc-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="1ccdc-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ccdc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ccdc-109">DESCRIPTION</span></span>
<span data-ttu-id="1ccdc-110">Mit dem Cmdlet **New-AzureRmSiteRecoveryReplicationProtectedItem** wird ein neues geschütztes Replikat Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="1ccdc-111">Verwenden Sie dieses Cmdlet, um die Replikation für ein geschütztes Element zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="1ccdc-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ccdc-112">EXAMPLES</span></span>

## <span data-ttu-id="1ccdc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ccdc-113">PARAMETERS</span></span>

### <span data-ttu-id="1ccdc-114">-Name</span><span class="sxs-lookup"><span data-stu-id="1ccdc-114">-Name</span></span>
<span data-ttu-id="1ccdc-115">Gibt den Namen des geschützten Elements Azure Site Recovery Replication an.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-116">-OS</span><span class="sxs-lookup"><span data-stu-id="1ccdc-116">-OS</span></span>
<span data-ttu-id="1ccdc-117">Gibt die Betriebssystemfamilie an.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-117">Specifies the operating system family.</span></span>
<span data-ttu-id="1ccdc-118">Die akzeptablen Werte für diesen Parameter sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="1ccdc-119">-OSDiskName</span></span>
<span data-ttu-id="1ccdc-120">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1ccdc-121">-ProtectableItem</span></span>
<span data-ttu-id="1ccdc-122">Gibt das zu schützende Azure Site Recovery-Element an.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1ccdc-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="1ccdc-124">Gibt das Azure Site Recovery Protection-Container Zuordnungsobjekt an, das für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1ccdc-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="1ccdc-126">Gibt die ID des Azure Storage-Kontos an, zu dem dieses Cmdlet repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1ccdc-127">-WaitForCompletion</span></span>
<span data-ttu-id="1ccdc-128">Gibt an, dass das Cmdlet auf den Abschluss wartet.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-128">Indicates that the cmdlet waits for completion.</span></span>

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

### <span data-ttu-id="1ccdc-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ccdc-129">-Confirm</span></span>
<span data-ttu-id="1ccdc-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ccdc-131">-WhatIf</span></span>
<span data-ttu-id="1ccdc-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1ccdc-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccdc-134">-DefaultProfile</span></span>
<span data-ttu-id="1ccdc-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccdc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccdc-136">CommonParameters</span></span>
<span data-ttu-id="1ccdc-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccdc-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ccdc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccdc-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ccdc-139">INPUTS</span></span>

### <span data-ttu-id="1ccdc-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1ccdc-140">ASRProtectableItem</span></span>
<span data-ttu-id="1ccdc-141">Der Parameter "ProtectableItem" akzeptiert den Wert vom Typ "ASRProtectableItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ccdc-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="1ccdc-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ccdc-142">OUTPUTS</span></span>

### <span data-ttu-id="1ccdc-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1ccdc-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1ccdc-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ccdc-144">NOTES</span></span>

## <span data-ttu-id="1ccdc-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ccdc-145">RELATED LINKS</span></span>

[<span data-ttu-id="1ccdc-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ccdc-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="1ccdc-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ccdc-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="1ccdc-148">Satz-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1ccdc-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
