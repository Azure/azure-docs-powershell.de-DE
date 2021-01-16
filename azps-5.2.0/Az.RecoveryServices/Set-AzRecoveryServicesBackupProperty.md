---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 27b783234f9f38f7445940ceb9969b6bc7fb6273
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357424"
---
# <span data-ttu-id="e54f0-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="e54f0-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="e54f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e54f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e54f0-103">Legt die Eigenschaften für die Sicherungsverwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="e54f0-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="e54f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e54f0-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e54f0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e54f0-105">DESCRIPTION</span></span>
<span data-ttu-id="e54f0-106">Das **Cmdlet "Set-AzRecoveryServicesBackupProperty"** legt sicherungsspeichereigenschaften für einen Wiederherstellungsdiensttresor fest.</span><span class="sxs-lookup"><span data-stu-id="e54f0-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="e54f0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e54f0-107">EXAMPLES</span></span>

### <span data-ttu-id="e54f0-108">Beispiel 1: Festlegen des Speichers von GeoRedundant für einen Tresor</span><span class="sxs-lookup"><span data-stu-id="e54f0-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="e54f0-109">Der erste Befehl ruft den Tresor namens "TestVault" ab und speichert ihn dann in der $Vault 01-Variable.</span><span class="sxs-lookup"><span data-stu-id="e54f0-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="e54f0-110">Der zweite Befehl legt die Sicherungsspeicherredundanz für $Vault 01 auf GeoRedundant fest.</span><span class="sxs-lookup"><span data-stu-id="e54f0-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="e54f0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e54f0-111">PARAMETERS</span></span>

### <span data-ttu-id="e54f0-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="e54f0-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="e54f0-113">Gibt den Typ der Sicherungsspeicherredundanz an.</span><span class="sxs-lookup"><span data-stu-id="e54f0-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e54f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54f0-114">-DefaultProfile</span></span>
<span data-ttu-id="e54f0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e54f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e54f0-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="e54f0-116">-Vault</span></span>
<span data-ttu-id="e54f0-117">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="e54f0-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="e54f0-118">Der Tresor muss ein **AzureRmRecoveryServicesVault-Objekt** sein.</span><span class="sxs-lookup"><span data-stu-id="e54f0-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="e54f0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e54f0-119">-Confirm</span></span>
<span data-ttu-id="e54f0-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e54f0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e54f0-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e54f0-121">-WhatIf</span></span>
<span data-ttu-id="e54f0-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e54f0-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="e54f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54f0-123">CommonParameters</span></span>
<span data-ttu-id="e54f0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e54f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54f0-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e54f0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54f0-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e54f0-126">INPUTS</span></span>

### <span data-ttu-id="e54f0-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="e54f0-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e54f0-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e54f0-128">OUTPUTS</span></span>

### <span data-ttu-id="e54f0-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="e54f0-129">System.Void</span></span>

## <span data-ttu-id="e54f0-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e54f0-130">NOTES</span></span>

## <span data-ttu-id="e54f0-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e54f0-131">RELATED LINKS</span></span>

[<span data-ttu-id="e54f0-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="e54f0-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="e54f0-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e54f0-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


