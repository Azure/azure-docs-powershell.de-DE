---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotdiskencryptionkey
schema: 2.0.0
ms.openlocfilehash: f78b680f5872301236c5d001ce9920d2edd61f02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848516"
---
# <span data-ttu-id="d6351-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d6351-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="d6351-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6351-102">SYNOPSIS</span></span>
<span data-ttu-id="d6351-103">Legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="d6351-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6351-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6351-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6351-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6351-105">DESCRIPTION</span></span>
<span data-ttu-id="d6351-106">Das Cmdlet " **Set-AzureRmSnapshotDiskEncryptionKey** " legt die Eigenschaften des Datenträger Verschlüsselungsschlüssels für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="d6351-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="d6351-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6351-107">EXAMPLES</span></span>

### <span data-ttu-id="d6351-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6351-108">Example 1</span></span>
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

<span data-ttu-id="d6351-109">Der erste Befehl erstellt ein lokales leeres snapshotobjekt mit der Größe 5GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="d6351-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="d6351-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6351-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d6351-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="d6351-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="d6351-112">Der letzte Befehl übernimmt das Snapshot-Objekt und erstellt einen Schnappschuss mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d6351-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d6351-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6351-113">PARAMETERS</span></span>

### <span data-ttu-id="d6351-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6351-114">-DefaultProfile</span></span>
<span data-ttu-id="d6351-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6351-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6351-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="d6351-116">-SecretUrl</span></span>
<span data-ttu-id="d6351-117">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="d6351-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="d6351-118">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="d6351-118">-Snapshot</span></span>
<span data-ttu-id="d6351-119">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d6351-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6351-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d6351-120">-SourceVaultId</span></span>
<span data-ttu-id="d6351-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="d6351-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="d6351-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6351-122">-Confirm</span></span>
<span data-ttu-id="d6351-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6351-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6351-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6351-124">-WhatIf</span></span>
<span data-ttu-id="d6351-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6351-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6351-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6351-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6351-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6351-127">CommonParameters</span></span>
<span data-ttu-id="d6351-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6351-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6351-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6351-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6351-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6351-130">INPUTS</span></span>

### <span data-ttu-id="d6351-131">Microsoft. Azure. Management. Compute. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="d6351-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="d6351-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d6351-132">System.String</span></span>

## <span data-ttu-id="d6351-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6351-133">OUTPUTS</span></span>

### <span data-ttu-id="d6351-134">Microsoft. Azure. Management. Compute. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="d6351-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="d6351-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6351-135">NOTES</span></span>

## <span data-ttu-id="d6351-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6351-136">RELATED LINKS</span></span>

