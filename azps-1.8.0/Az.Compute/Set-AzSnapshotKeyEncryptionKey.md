---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 6e5c81e138f016ffef4361e5b9f79e16b051b016
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661452"
---
# <span data-ttu-id="febcc-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="febcc-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="febcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="febcc-102">SYNOPSIS</span></span>
<span data-ttu-id="febcc-103">Legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="febcc-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="febcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="febcc-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="febcc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="febcc-105">DESCRIPTION</span></span>
<span data-ttu-id="febcc-106">Das Cmdlet " **Set-AzSnapshotKeyEncryptionKey** " legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="febcc-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="febcc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="febcc-107">EXAMPLES</span></span>

### <span data-ttu-id="febcc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="febcc-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="febcc-109">Der erste Befehl erstellt ein lokales leeres snapshotobjekt mit der Größe 5GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="febcc-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="febcc-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="febcc-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="febcc-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="febcc-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="febcc-112">Der letzte Befehl übernimmt das Snapshot-Objekt und erstellt einen Schnappschuss mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="febcc-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="febcc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="febcc-113">PARAMETERS</span></span>

### <span data-ttu-id="febcc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febcc-114">-DefaultProfile</span></span>
<span data-ttu-id="febcc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="febcc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="febcc-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="febcc-116">-KeyUrl</span></span>
<span data-ttu-id="febcc-117">Gibt an die Schlüssel-URL.</span><span class="sxs-lookup"><span data-stu-id="febcc-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="febcc-118">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="febcc-118">-Snapshot</span></span>
<span data-ttu-id="febcc-119">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="febcc-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="febcc-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="febcc-120">-SourceVaultId</span></span>
<span data-ttu-id="febcc-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="febcc-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="febcc-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="febcc-122">-Confirm</span></span>
<span data-ttu-id="febcc-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="febcc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="febcc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="febcc-124">-WhatIf</span></span>
<span data-ttu-id="febcc-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="febcc-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="febcc-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="febcc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="febcc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febcc-127">CommonParameters</span></span>
<span data-ttu-id="febcc-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febcc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febcc-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febcc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febcc-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="febcc-130">INPUTS</span></span>

### <span data-ttu-id="febcc-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="febcc-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="febcc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="febcc-132">System.String</span></span>

## <span data-ttu-id="febcc-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="febcc-133">OUTPUTS</span></span>

### <span data-ttu-id="febcc-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="febcc-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="febcc-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="febcc-135">NOTES</span></span>

## <span data-ttu-id="febcc-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="febcc-136">RELATED LINKS</span></span>
