---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296872"
---
# <span data-ttu-id="df559-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="df559-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="df559-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df559-102">SYNOPSIS</span></span>
<span data-ttu-id="df559-103">Sichern eines Schlüssels in einem verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="df559-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="df559-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df559-104">SYNTAX</span></span>

### <span data-ttu-id="df559-105">ByKeyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="df559-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df559-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="df559-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df559-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df559-107">DESCRIPTION</span></span>
<span data-ttu-id="df559-108">Das Cmdlet **Backup-AzManagedHsmKey** sichern einen angegebenen Schlüssel in einem verwalteten HSM, indem Sie es herunterladen und in einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="df559-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="df559-109">Wenn mehrere Versionen des Schlüssels vorhanden sind, werden alle Versionen in die Sicherung aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="df559-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="df559-110">Da der heruntergeladene Inhalt verschlüsselt ist, kann er nicht außerhalb von Azure Managed HSM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df559-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="df559-111">Sie können einen gesicherten Schlüssel für ein verwaltetes HSM im Abonnement wiederherstellen, von dem es gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="df559-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="df559-112">Typische Gründe für die Verwendung dieses Cmdlets sind:</span><span class="sxs-lookup"><span data-stu-id="df559-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="df559-113">Sie möchten eine Kopie Ihres Schlüssels hinterlegen, damit Sie eine Offlinekopie haben, falls Sie Ihren Schlüssel versehentlich in Ihrem Managed HSM löschen.</span><span class="sxs-lookup"><span data-stu-id="df559-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="df559-114">Sie haben einen Schlüssel mit verwaltetem HSM erstellt und möchten nun den Schlüssel in einen anderen Azure-Bereich Klonen, sodass Sie ihn aus allen Instanzen ihrer verteilten Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="df559-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="df559-115">Verwenden Sie das Cmdlet **Backup-AzManagedHsmKey** , um den Schlüssel im verschlüsselten Format abzurufen, und verwenden Sie dann das Restore-AzManagedHsmKey-Cmdlet, und geben Sie im zweiten Bereich ein verwaltetes HSM an.</span><span class="sxs-lookup"><span data-stu-id="df559-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="df559-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df559-116">EXAMPLES</span></span>

### <span data-ttu-id="df559-117">Beispiel 1: Sichern eines Schlüssels mit einem automatisch generierten Dateinamen</span><span class="sxs-lookup"><span data-stu-id="df559-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="df559-118">Dieser Befehl ruft den Schlüssel mit dem Namen TestKey aus dem verwalteten HSM mit dem Namen testmhsm ab und speichert eine Sicherungskopie dieses Schlüssels in einer Datei, die automatisch nach ihnen benannt wird, und zeigt den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="df559-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="df559-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="df559-119">PARAMETERS</span></span>

### <span data-ttu-id="df559-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df559-120">-DefaultProfile</span></span>
<span data-ttu-id="df559-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df559-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df559-122">-Force</span><span class="sxs-lookup"><span data-stu-id="df559-122">-Force</span></span>
<span data-ttu-id="df559-123">Überschreiben der angegebenen Datei, sofern vorhanden</span><span class="sxs-lookup"><span data-stu-id="df559-123">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="df559-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="df559-124">-HsmName</span></span>
<span data-ttu-id="df559-125">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="df559-125">HSM name.</span></span> <span data-ttu-id="df559-126">Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="df559-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df559-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df559-127">-InputObject</span></span>
<span data-ttu-id="df559-128">Schlüsselpaket, das von der Ausgabe eines Abruf Anrufs in eine Sicherungskopie geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="df559-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df559-129">-Name</span><span class="sxs-lookup"><span data-stu-id="df559-129">-Name</span></span>
<span data-ttu-id="df559-130">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="df559-130">Key name.</span></span>
<span data-ttu-id="df559-131">Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="df559-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df559-132">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="df559-132">-OutputFile</span></span>
<span data-ttu-id="df559-133">Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="df559-133">Output file.</span></span>
<span data-ttu-id="df559-134">Die Ausgabedatei, in der der gesicherte Schlüssel BLOB gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="df559-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="df559-135">Wenn diese nicht vorhanden ist, wird ein Standarddateiname ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="df559-135">If not present, a default filename is chosen.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df559-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df559-136">-Confirm</span></span>
<span data-ttu-id="df559-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df559-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df559-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df559-138">-WhatIf</span></span>
<span data-ttu-id="df559-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df559-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df559-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df559-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df559-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df559-141">CommonParameters</span></span>
<span data-ttu-id="df559-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df559-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df559-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df559-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df559-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df559-144">INPUTS</span></span>

### <span data-ttu-id="df559-145">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="df559-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="df559-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df559-146">OUTPUTS</span></span>

### <span data-ttu-id="df559-147">System. String</span><span class="sxs-lookup"><span data-stu-id="df559-147">System.String</span></span>

## <span data-ttu-id="df559-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="df559-148">NOTES</span></span>

## <span data-ttu-id="df559-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df559-149">RELATED LINKS</span></span>

[<span data-ttu-id="df559-150">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="df559-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="df559-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="df559-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="df559-152">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="df559-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="df559-153">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="df559-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="df559-154">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="df559-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="df559-155">Wiederherstellen – AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="df559-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)