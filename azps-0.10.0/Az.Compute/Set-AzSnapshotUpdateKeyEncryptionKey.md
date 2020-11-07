---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: 8b1fa88954c95c8f49af4767e353bba5a42e3a92
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844263"
---
# <span data-ttu-id="7f2c1-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7f2c1-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="7f2c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f2c1-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2c1-103">Legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Aktualisierungs Objekt für Snapshots fest.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="7f2c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f2c1-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f2c1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f2c1-105">DESCRIPTION</span></span>
<span data-ttu-id="7f2c1-106">Das Cmdlet " **Set-AzSnapshotUpdateKeyEncryptionKey** " legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Aktualisierungs Objekt für Snapshots fest.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="7f2c1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f2c1-107">EXAMPLES</span></span>

### <span data-ttu-id="7f2c1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f2c1-108">Example 1</span></span>
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

<span data-ttu-id="7f2c1-109">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="7f2c1-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="7f2c1-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="7f2c1-112">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7f2c1-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7f2c1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f2c1-113">PARAMETERS</span></span>

### <span data-ttu-id="7f2c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2c1-114">-DefaultProfile</span></span>
<span data-ttu-id="7f2c1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f2c1-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="7f2c1-116">-KeyUrl</span></span>
<span data-ttu-id="7f2c1-117">Gibt an die Schlüssel-URL.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-117">Specifes the key Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2c1-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="7f2c1-118">-SnapshotUpdate</span></span>
<span data-ttu-id="7f2c1-119">Gibt ein lokales Aktualisierungs Objekt für Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2c1-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="7f2c1-120">-SourceVaultId</span></span>
<span data-ttu-id="7f2c1-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-121">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2c1-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f2c1-122">-Confirm</span></span>
<span data-ttu-id="7f2c1-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2c1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2c1-124">-WhatIf</span></span>
<span data-ttu-id="7f2c1-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f2c1-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2c1-127">CommonParameters</span></span>
<span data-ttu-id="7f2c1-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f2c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2c1-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f2c1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2c1-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f2c1-130">INPUTS</span></span>

### <span data-ttu-id="7f2c1-131">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="7f2c1-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="7f2c1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7f2c1-132">System.String</span></span>

## <span data-ttu-id="7f2c1-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f2c1-133">OUTPUTS</span></span>

### <span data-ttu-id="7f2c1-134">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="7f2c1-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="7f2c1-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f2c1-135">NOTES</span></span>

## <span data-ttu-id="7f2c1-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f2c1-136">RELATED LINKS</span></span>

