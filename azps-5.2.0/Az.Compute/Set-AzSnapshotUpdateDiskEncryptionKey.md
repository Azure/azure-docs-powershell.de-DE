---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304003"
---
# <span data-ttu-id="a69ba-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a69ba-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="a69ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a69ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a69ba-103">Legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Snapshotaktualisierungsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="a69ba-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="a69ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a69ba-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a69ba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a69ba-105">DESCRIPTION</span></span>
<span data-ttu-id="a69ba-106">Das **Cmdlet Set-AzSnapshotUpdateDiskEncryptionKey** legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Snapshotaktualisierungsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="a69ba-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="a69ba-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a69ba-107">EXAMPLES</span></span>

### <span data-ttu-id="a69ba-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a69ba-108">Example 1</span></span>
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

<span data-ttu-id="a69ba-109">Der erste Befehl erstellt ein lokales leeres Snapshotupdateobjekt mit einer Größe von 10 GB im Premium_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="a69ba-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a69ba-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a69ba-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a69ba-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Snapshotupdateobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a69ba-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="a69ba-112">Der letzte Befehl erstellt das Snapshotaktualisierungsobjekt und aktualisiert eine vorhandene Momentaufnahme mit dem Namen 'Snapshot01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="a69ba-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a69ba-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a69ba-113">PARAMETERS</span></span>

### <span data-ttu-id="a69ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69ba-114">-DefaultProfile</span></span>
<span data-ttu-id="a69ba-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a69ba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a69ba-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="a69ba-116">-SecretUrl</span></span>
<span data-ttu-id="a69ba-117">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="a69ba-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="a69ba-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a69ba-118">-SnapshotUpdate</span></span>
<span data-ttu-id="a69ba-119">Gibt ein lokales Snapshotaktualisierungsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="a69ba-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="a69ba-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a69ba-120">-SourceVaultId</span></span>
<span data-ttu-id="a69ba-121">Gibt die Quelltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="a69ba-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="a69ba-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a69ba-122">-Confirm</span></span>
<span data-ttu-id="a69ba-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a69ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a69ba-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a69ba-124">-WhatIf</span></span>
<span data-ttu-id="a69ba-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a69ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a69ba-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a69ba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a69ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69ba-127">CommonParameters</span></span>
<span data-ttu-id="a69ba-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69ba-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a69ba-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69ba-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a69ba-130">INPUTS</span></span>

### <span data-ttu-id="a69ba-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a69ba-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="a69ba-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a69ba-132">System.String</span></span>

## <span data-ttu-id="a69ba-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a69ba-133">OUTPUTS</span></span>

### <span data-ttu-id="a69ba-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a69ba-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="a69ba-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a69ba-135">NOTES</span></span>

## <span data-ttu-id="a69ba-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a69ba-136">RELATED LINKS</span></span>
