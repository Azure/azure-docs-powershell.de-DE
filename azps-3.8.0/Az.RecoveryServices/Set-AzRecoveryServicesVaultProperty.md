---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003727"
---
# <span data-ttu-id="c680e-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="c680e-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="c680e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c680e-102">SYNOPSIS</span></span>
<span data-ttu-id="c680e-103">Aktualisiert die Eigenschaften eines Tresors.</span><span class="sxs-lookup"><span data-stu-id="c680e-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="c680e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c680e-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c680e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c680e-105">DESCRIPTION</span></span>
<span data-ttu-id="c680e-106">Das Cmdlet " **Satz-AzRecoveryServicesVaultProperty** " aktualisiert die Eigenschaften eines Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="c680e-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="c680e-107">Sie können das Cmdlet " **Satz-AzRecoveryServicesVaultProperty** " verwenden, um die aktuellen Eigenschaften eines Tresors abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c680e-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="c680e-108">Mithilfe dieses Cmdlets kann die **SoftDeleteFeatureState** -Eigenschaft eines Tresors zu einem beliebigen Zeitpunkt aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c680e-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="c680e-109">Die **SoftDeleteFeatureState** -Eigenschaft eines Tresors kann nur deaktiviert werden, wenn im Tresor keine registrierten Container vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c680e-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="c680e-110">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="c680e-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c680e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c680e-111">EXAMPLES</span></span>

### <span data-ttu-id="c680e-112">Beispiel 1: Aktualisieren der SoftDeleteFeatureState eines Tresors</span><span class="sxs-lookup"><span data-stu-id="c680e-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="c680e-113">Der erste Befehl ruft ein Vault-Objekt ab und speichert es dann in der $Vault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c680e-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="c680e-114">Der zweite Befehl aktualisiert die SoftDeleteFeatureState-Eigenschaft des Tresors in den Zustand "aktiviert".</span><span class="sxs-lookup"><span data-stu-id="c680e-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="c680e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c680e-115">PARAMETERS</span></span>

### <span data-ttu-id="c680e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c680e-116">-DefaultProfile</span></span>
<span data-ttu-id="c680e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c680e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c680e-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="c680e-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="c680e-119">SoftDeleteFeatureState des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="c680e-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c680e-120">-Tresor</span><span class="sxs-lookup"><span data-stu-id="c680e-120">-VaultId</span></span>
<span data-ttu-id="c680e-121">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="c680e-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c680e-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c680e-122">-Confirm</span></span>
<span data-ttu-id="c680e-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c680e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c680e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c680e-124">-WhatIf</span></span>
<span data-ttu-id="c680e-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c680e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c680e-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c680e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c680e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c680e-127">CommonParameters</span></span>
<span data-ttu-id="c680e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c680e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c680e-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c680e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c680e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c680e-130">INPUTS</span></span>

### <span data-ttu-id="c680e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c680e-131">System.String</span></span>

### <span data-ttu-id="c680e-132">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="c680e-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="c680e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c680e-133">OUTPUTS</span></span>

### <span data-ttu-id="c680e-134">Microsoft. Azure. Management. RecoveryServices. Backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="c680e-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="c680e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c680e-135">NOTES</span></span>

## <span data-ttu-id="c680e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c680e-136">RELATED LINKS</span></span>

[<span data-ttu-id="c680e-137">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="c680e-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="c680e-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="c680e-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


