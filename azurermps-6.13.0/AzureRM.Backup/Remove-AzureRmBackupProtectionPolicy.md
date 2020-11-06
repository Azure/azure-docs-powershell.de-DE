---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: b7eaa3ef0c0379a0799e4091a4e808415b2f9fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480585"
---
# <span data-ttu-id="8099a-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8099a-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="8099a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8099a-102">SYNOPSIS</span></span>
<span data-ttu-id="8099a-103">Löscht eine Richtlinie aus einem Sicherungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8099a-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8099a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8099a-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8099a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8099a-105">DESCRIPTION</span></span>
<span data-ttu-id="8099a-106">Das Cmdlet **Remove-AzureRmBackupProtectionPolicy** löscht eine Richtlinie aus einem Azure Backup Vault.</span><span class="sxs-lookup"><span data-stu-id="8099a-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>
<span data-ttu-id="8099a-107">Bevor Sie eine Sicherungsschutz Richtlinie löschen können, darf die Richtlinie keine zugeordneten Sicherungselemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="8099a-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="8099a-108">Bevor Sie die Richtlinie löschen, stellen Sie sicher, dass jedes zugeordnete Element einer anderen Richtlinie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8099a-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="8099a-109">Verwenden Sie das Enable-AzureRmBackupProtection-Cmdlet, um eine andere Richtlinie einem Sicherungselement zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="8099a-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="8099a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8099a-110">EXAMPLES</span></span>

### <span data-ttu-id="8099a-111">Beispiel 1: Entfernen einer Sicherungsschutz Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8099a-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="8099a-112">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="8099a-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="8099a-113">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="8099a-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="8099a-114">Der zweite Befehl erstellt eine Aufbewahrungsrichtlinie für 30 Tage tägliche Aufbewahrung und speichert Sie dann in der $Daily-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8099a-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="8099a-115">Der zweite Befehl ruft die Schutzrichtlinie mit dem Namen DailyBackup im Tresor in $Vault mit dem Cmdlet **Get-AzureRmBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="8099a-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="8099a-116">Der Befehl übergibt die Richtlinie an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8099a-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="8099a-117">Dieses Cmdlet entfernt die Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8099a-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="8099a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="8099a-118">PARAMETERS</span></span>

### <span data-ttu-id="8099a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8099a-119">-DefaultProfile</span></span>
<span data-ttu-id="8099a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8099a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8099a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8099a-121">-Force</span></span>
<span data-ttu-id="8099a-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8099a-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8099a-123">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8099a-123">-ProtectionPolicy</span></span>
<span data-ttu-id="8099a-124">Gibt die von diesem Cmdlet entfernte Schutzrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="8099a-124">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="8099a-125">Verwenden des Get-AzureRmBackupProtectionPolicy-Cmdlets zum Abrufen eines **AzureRmBackupProtectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="8099a-125">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8099a-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8099a-126">-Confirm</span></span>
<span data-ttu-id="8099a-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8099a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8099a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8099a-128">-WhatIf</span></span>
<span data-ttu-id="8099a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8099a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8099a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8099a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8099a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8099a-131">CommonParameters</span></span>
<span data-ttu-id="8099a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8099a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8099a-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8099a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8099a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8099a-134">INPUTS</span></span>

### <span data-ttu-id="8099a-135">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8099a-135">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="8099a-136">Parameter: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8099a-136">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="8099a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8099a-137">OUTPUTS</span></span>

### <span data-ttu-id="8099a-138">System. void</span><span class="sxs-lookup"><span data-stu-id="8099a-138">System.Void</span></span>

## <span data-ttu-id="8099a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="8099a-139">NOTES</span></span>

## <span data-ttu-id="8099a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8099a-140">RELATED LINKS</span></span>

[<span data-ttu-id="8099a-141">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8099a-141">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="8099a-142">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8099a-142">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="8099a-143">Neu – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8099a-143">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


