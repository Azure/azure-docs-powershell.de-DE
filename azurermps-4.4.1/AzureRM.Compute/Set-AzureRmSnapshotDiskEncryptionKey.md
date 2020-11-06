---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
ms.openlocfilehash: 8f31d238a01ff08faadcb8189b771a8da4c883ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501930"
---
# <span data-ttu-id="b247d-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b247d-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="b247d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b247d-102">SYNOPSIS</span></span>
<span data-ttu-id="b247d-103">Legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="b247d-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b247d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b247d-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b247d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b247d-105">DESCRIPTION</span></span>
<span data-ttu-id="b247d-106">Das Cmdlet " **Set-AzureRmSnapshotDiskEncryptionKey** " legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="b247d-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="b247d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b247d-107">EXAMPLES</span></span>

### <span data-ttu-id="b247d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b247d-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="b247d-109">Der erste Befehl erstellt ein lokales leeres snapshotobjekt mit der Größe 5GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="b247d-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="b247d-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b247d-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b247d-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="b247d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="b247d-112">Der letzte Befehl übernimmt das Snapshot-Objekt und erstellt einen Schnappschuss mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b247d-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b247d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b247d-113">PARAMETERS</span></span>

### <span data-ttu-id="b247d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b247d-114">-DefaultProfile</span></span>
<span data-ttu-id="b247d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b247d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b247d-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="b247d-116">-SecretUrl</span></span>
<span data-ttu-id="b247d-117">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="b247d-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="b247d-118">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="b247d-118">-Snapshot</span></span>
<span data-ttu-id="b247d-119">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b247d-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b247d-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b247d-120">-SourceVaultId</span></span>
<span data-ttu-id="b247d-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="b247d-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="b247d-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b247d-122">-Confirm</span></span>
<span data-ttu-id="b247d-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b247d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b247d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b247d-124">-WhatIf</span></span>
<span data-ttu-id="b247d-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b247d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b247d-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b247d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b247d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b247d-127">CommonParameters</span></span>
<span data-ttu-id="b247d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b247d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b247d-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b247d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b247d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b247d-130">INPUTS</span></span>

### <span data-ttu-id="b247d-131">Microsoft. Azure. Management. Compute. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="b247d-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="b247d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b247d-132">System.String</span></span>

## <span data-ttu-id="b247d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b247d-133">OUTPUTS</span></span>

### <span data-ttu-id="b247d-134">Microsoft. Azure. Management. Compute. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="b247d-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="b247d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b247d-135">NOTES</span></span>

## <span data-ttu-id="b247d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b247d-136">RELATED LINKS</span></span>

