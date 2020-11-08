---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175907"
---
# <span data-ttu-id="6b2a4-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="6b2a4-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="6b2a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2a4-103">Aktualisiert die Eigenschaften eines Tresors.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="6b2a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b2a4-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b2a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b2a4-105">DESCRIPTION</span></span>
<span data-ttu-id="6b2a4-106">Das Cmdlet " **Satz-AzRecoveryServicesVaultProperty** " aktualisiert die Eigenschaften eines Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="6b2a4-107">Dieses Cmdlet gibt die aktualisierten Vault-Eigenschaften nach dem aktuellen Mengen Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="6b2a4-108">Die Verwendung dieser Cmdlet-Eigenschaften von Vault wie Soft-Delete kann zu einem beliebigen Zeitpunkt aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="6b2a4-109">Die **SoftDeleteFeatureState** -Eigenschaft eines Tresors kann nur deaktiviert werden, wenn im Tresor keine registrierten Container vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="6b2a4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b2a4-110">EXAMPLES</span></span>

### <span data-ttu-id="6b2a4-111">Beispiel 1: Aktualisieren der SoftDeleteFeatureState eines Tresors</span><span class="sxs-lookup"><span data-stu-id="6b2a4-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="6b2a4-112">Der erste Befehl ruft ein Vault-Objekt ab und speichert es dann in der $Vault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="6b2a4-113">Der zweite Befehl aktualisiert die SoftDeleteFeatureState-Eigenschaft des Tresors in den Zustand "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="6b2a4-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="6b2a4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b2a4-114">PARAMETERS</span></span>

### <span data-ttu-id="6b2a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2a4-115">-DefaultProfile</span></span>
<span data-ttu-id="6b2a4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b2a4-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="6b2a4-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="6b2a4-118">SoftDeleteFeatureState des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="6b2a4-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2a4-119">-Tresor</span><span class="sxs-lookup"><span data-stu-id="6b2a4-119">-VaultId</span></span>
<span data-ttu-id="6b2a4-120">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="6b2a4-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2a4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b2a4-121">-Confirm</span></span>
<span data-ttu-id="6b2a4-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b2a4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b2a4-123">-WhatIf</span></span>
<span data-ttu-id="6b2a4-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="6b2a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2a4-125">CommonParameters</span></span>
<span data-ttu-id="6b2a4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b2a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2a4-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b2a4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2a4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b2a4-128">INPUTS</span></span>

### <span data-ttu-id="6b2a4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6b2a4-129">System.String</span></span>

### <span data-ttu-id="6b2a4-130">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="6b2a4-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="6b2a4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b2a4-131">OUTPUTS</span></span>

### <span data-ttu-id="6b2a4-132">Microsoft. Azure. Management. RecoveryServices. Backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="6b2a4-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="6b2a4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b2a4-133">NOTES</span></span>

## <span data-ttu-id="6b2a4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b2a4-134">RELATED LINKS</span></span>

[<span data-ttu-id="6b2a4-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6b2a4-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="6b2a4-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="6b2a4-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


