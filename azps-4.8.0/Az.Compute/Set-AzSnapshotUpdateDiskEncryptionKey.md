---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009985"
---
# <span data-ttu-id="e6111-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e6111-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="e6111-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6111-102">SYNOPSIS</span></span>
<span data-ttu-id="e6111-103">Legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Aktualisierungs Objekt für Snapshots fest.</span><span class="sxs-lookup"><span data-stu-id="e6111-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="e6111-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6111-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6111-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6111-105">DESCRIPTION</span></span>
<span data-ttu-id="e6111-106">Das Cmdlet " **Set-AzSnapshotUpdateDiskEncryptionKey** " legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Aktualisierungs Objekt für Snapshots fest.</span><span class="sxs-lookup"><span data-stu-id="e6111-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="e6111-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6111-107">EXAMPLES</span></span>

### <span data-ttu-id="e6111-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6111-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="e6111-109">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="e6111-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e6111-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e6111-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e6111-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="e6111-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="e6111-112">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e6111-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e6111-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6111-113">PARAMETERS</span></span>

### <span data-ttu-id="e6111-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6111-114">-DefaultProfile</span></span>
<span data-ttu-id="e6111-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6111-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6111-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="e6111-116">-SecretUrl</span></span>
<span data-ttu-id="e6111-117">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="e6111-117">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6111-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="e6111-118">-SnapshotUpdate</span></span>
<span data-ttu-id="e6111-119">Gibt ein lokales Aktualisierungs Objekt für Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="e6111-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6111-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e6111-120">-SourceVaultId</span></span>
<span data-ttu-id="e6111-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="e6111-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6111-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6111-122">-Confirm</span></span>
<span data-ttu-id="e6111-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6111-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6111-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6111-124">-WhatIf</span></span>
<span data-ttu-id="e6111-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6111-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6111-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6111-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6111-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6111-127">CommonParameters</span></span>
<span data-ttu-id="e6111-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6111-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6111-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6111-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6111-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6111-130">INPUTS</span></span>

### <span data-ttu-id="e6111-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="e6111-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="e6111-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e6111-132">System.String</span></span>

## <span data-ttu-id="e6111-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6111-133">OUTPUTS</span></span>

### <span data-ttu-id="e6111-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="e6111-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="e6111-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6111-135">NOTES</span></span>

## <span data-ttu-id="e6111-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6111-136">RELATED LINKS</span></span>
