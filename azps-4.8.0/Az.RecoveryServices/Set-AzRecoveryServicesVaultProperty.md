---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174219"
---
# <span data-ttu-id="ffab6-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="ffab6-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="ffab6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffab6-102">SYNOPSIS</span></span>
<span data-ttu-id="ffab6-103">Aktualisiert die Eigenschaften eines Tresors.</span><span class="sxs-lookup"><span data-stu-id="ffab6-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="ffab6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffab6-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffab6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffab6-105">DESCRIPTION</span></span>
<span data-ttu-id="ffab6-106">Das Cmdlet " **Satz-AzRecoveryServicesVaultProperty** " aktualisiert die Eigenschaften eines Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="ffab6-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="ffab6-107">Dieses Cmdlet gibt die aktualisierten Vault-Eigenschaften nach dem aktuellen Mengen Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="ffab6-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="ffab6-108">Die Verwendung dieser Cmdlet-Eigenschaften von Vault wie Soft-Delete kann zu einem beliebigen Zeitpunkt aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ffab6-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="ffab6-109">Die **SoftDeleteFeatureState** -Eigenschaft eines Tresors kann nur deaktiviert werden, wenn im Tresor keine registrierten Container vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ffab6-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="ffab6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffab6-110">EXAMPLES</span></span>

### <span data-ttu-id="ffab6-111">Beispiel 1: Aktualisieren der SoftDeleteFeatureState eines Tresors</span><span class="sxs-lookup"><span data-stu-id="ffab6-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="ffab6-112">Der erste Befehl ruft ein Vault-Objekt ab und speichert es dann in der $Vault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ffab6-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="ffab6-113">Der zweite Befehl aktualisiert die SoftDeleteFeatureState-Eigenschaft des Tresors in den Zustand "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="ffab6-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="ffab6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffab6-114">PARAMETERS</span></span>

### <span data-ttu-id="ffab6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffab6-115">-DefaultProfile</span></span>
<span data-ttu-id="ffab6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffab6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffab6-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="ffab6-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="ffab6-118">SoftDeleteFeatureState des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="ffab6-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ffab6-119">-Tresor</span><span class="sxs-lookup"><span data-stu-id="ffab6-119">-VaultId</span></span>
<span data-ttu-id="ffab6-120">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="ffab6-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ffab6-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffab6-121">-Confirm</span></span>
<span data-ttu-id="ffab6-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffab6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffab6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffab6-123">-WhatIf</span></span>
<span data-ttu-id="ffab6-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffab6-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="ffab6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffab6-125">CommonParameters</span></span>
<span data-ttu-id="ffab6-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffab6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffab6-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffab6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffab6-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffab6-128">INPUTS</span></span>

### <span data-ttu-id="ffab6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ffab6-129">System.String</span></span>

### <span data-ttu-id="ffab6-130">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="ffab6-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="ffab6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffab6-131">OUTPUTS</span></span>

### <span data-ttu-id="ffab6-132">Microsoft. Azure. Management. RecoveryServices. Backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="ffab6-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="ffab6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffab6-133">NOTES</span></span>

## <span data-ttu-id="ffab6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffab6-134">RELATED LINKS</span></span>

[<span data-ttu-id="ffab6-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ffab6-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ffab6-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="ffab6-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


