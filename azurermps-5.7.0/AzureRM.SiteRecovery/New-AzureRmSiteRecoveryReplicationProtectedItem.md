---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 28b2f976b85d7db40cdb80cf2b9b58a2d7692952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502369"
---
# <span data-ttu-id="3319e-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3319e-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="3319e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3319e-102">SYNOPSIS</span></span>
<span data-ttu-id="3319e-103">Ermöglicht die Replikation für ein geschütztes Element durch Erstellen eines geschützten Elements.</span><span class="sxs-lookup"><span data-stu-id="3319e-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3319e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3319e-104">SYNTAX</span></span>

### <span data-ttu-id="3319e-105">Disabled (Standard)</span><span class="sxs-lookup"><span data-stu-id="3319e-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3319e-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="3319e-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3319e-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="3319e-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3319e-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="3319e-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3319e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3319e-109">DESCRIPTION</span></span>
<span data-ttu-id="3319e-110">Mit dem Cmdlet **New-AzureRmSiteRecoveryReplicationProtectedItem** wird ein neues geschütztes Replikat Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="3319e-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="3319e-111">Verwenden Sie dieses Cmdlet, um die Replikation für ein geschütztes Element zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3319e-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="3319e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3319e-112">EXAMPLES</span></span>

## <span data-ttu-id="3319e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3319e-113">PARAMETERS</span></span>

### <span data-ttu-id="3319e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3319e-114">-DefaultProfile</span></span>
<span data-ttu-id="3319e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3319e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3319e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3319e-116">-Name</span></span>
<span data-ttu-id="3319e-117">Gibt den Namen des geschützten Elements Azure Site Recovery Replication an.</span><span class="sxs-lookup"><span data-stu-id="3319e-117">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-118">-OS</span><span class="sxs-lookup"><span data-stu-id="3319e-118">-OS</span></span>
<span data-ttu-id="3319e-119">Gibt die Betriebssystemfamilie an.</span><span class="sxs-lookup"><span data-stu-id="3319e-119">Specifies the operating system family.</span></span>
<span data-ttu-id="3319e-120">Die akzeptablen Werte für diesen Parameter sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="3319e-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="3319e-121">-OSDiskName</span></span>
<span data-ttu-id="3319e-122">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="3319e-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3319e-123">-ProtectableItem</span></span>
<span data-ttu-id="3319e-124">Gibt das zu schützende Azure Site Recovery-Element an.</span><span class="sxs-lookup"><span data-stu-id="3319e-124">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3319e-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="3319e-126">Gibt das Azure Site Recovery Protection-Container Zuordnungsobjekt an, das für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3319e-126">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3319e-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="3319e-128">Gibt die ID des Azure Storage-Kontos an, zu dem dieses Cmdlet repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="3319e-128">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-129">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3319e-129">-WaitForCompletion</span></span>
<span data-ttu-id="3319e-130">Gibt an, dass das Cmdlet auf den Abschluss wartet.</span><span class="sxs-lookup"><span data-stu-id="3319e-130">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3319e-131">-Confirm</span></span>
<span data-ttu-id="3319e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3319e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3319e-133">-WhatIf</span></span>
<span data-ttu-id="3319e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3319e-134">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3319e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3319e-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3319e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3319e-136">CommonParameters</span></span>
<span data-ttu-id="3319e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3319e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3319e-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3319e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3319e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3319e-139">INPUTS</span></span>

### <span data-ttu-id="3319e-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3319e-140">ASRProtectableItem</span></span>
<span data-ttu-id="3319e-141">Der Parameter "ProtectableItem" akzeptiert den Wert vom Typ "ASRProtectableItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3319e-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="3319e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3319e-142">OUTPUTS</span></span>

### <span data-ttu-id="3319e-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3319e-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3319e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3319e-144">NOTES</span></span>

## <span data-ttu-id="3319e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3319e-145">RELATED LINKS</span></span>

[<span data-ttu-id="3319e-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3319e-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="3319e-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3319e-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="3319e-148">Satz-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3319e-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
