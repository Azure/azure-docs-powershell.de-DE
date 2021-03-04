---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 5e66fc57f6ee9daffde27226bc0321f415cc10d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942256"
---
# <span data-ttu-id="94ed0-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="94ed0-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="94ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="94ed0-103">Legt die Eigenschaften für die Sicherungsverwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="94ed0-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="94ed0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94ed0-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>  [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-EnableCrossRegionRestore] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94ed0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94ed0-105">DESCRIPTION</span></span>
<span data-ttu-id="94ed0-106">Das **Cmdlet Set-AzRecoveryServicesBackupProperty** legt Sicherungsspeichereigenschaften für einen Recovery Services-Tresor fest.</span><span class="sxs-lookup"><span data-stu-id="94ed0-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="94ed0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94ed0-107">EXAMPLES</span></span>

### <span data-ttu-id="94ed0-108">Beispiel 1: Festlegen von GeoRedundant-Speicher für einen Tresor</span><span class="sxs-lookup"><span data-stu-id="94ed0-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="94ed0-109">Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der $Vault 01-Variable.</span><span class="sxs-lookup"><span data-stu-id="94ed0-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="94ed0-110">Der zweite Befehl legt die Redundanz des Sicherungsspeichers für $Vault 01 auf GeoRedundant fest.</span><span class="sxs-lookup"><span data-stu-id="94ed0-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="94ed0-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="94ed0-111">PARAMETERS</span></span>

### <span data-ttu-id="94ed0-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="94ed0-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="94ed0-113">Gibt den Redundanztyp des Sicherungsspeichers an.</span><span class="sxs-lookup"><span data-stu-id="94ed0-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, ZoneRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ed0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ed0-114">-DefaultProfile</span></span>
<span data-ttu-id="94ed0-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94ed0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94ed0-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="94ed0-116">-Vault</span></span>
<span data-ttu-id="94ed0-117">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="94ed0-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="94ed0-118">Der Tresor muss ein **AzureRmRecoveryServicesVault-Objekt** sein.</span><span class="sxs-lookup"><span data-stu-id="94ed0-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94ed0-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94ed0-119">-Confirm</span></span>
<span data-ttu-id="94ed0-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94ed0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ed0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ed0-121">-WhatIf</span></span>
<span data-ttu-id="94ed0-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94ed0-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="94ed0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ed0-123">CommonParameters</span></span>
<span data-ttu-id="94ed0-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ed0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ed0-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94ed0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ed0-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94ed0-126">INPUTS</span></span>

### <span data-ttu-id="94ed0-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="94ed0-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="94ed0-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94ed0-128">OUTPUTS</span></span>

### <span data-ttu-id="94ed0-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="94ed0-129">System.Void</span></span>

## <span data-ttu-id="94ed0-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="94ed0-130">NOTES</span></span>

## <span data-ttu-id="94ed0-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="94ed0-131">RELATED LINKS</span></span>

[<span data-ttu-id="94ed0-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="94ed0-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="94ed0-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="94ed0-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


