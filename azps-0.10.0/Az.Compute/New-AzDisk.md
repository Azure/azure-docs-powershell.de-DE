---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1eea8504f974e7ffc504520a5b5abc036c4d3e2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844508"
---
# <span data-ttu-id="d8952-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="d8952-101">New-AzDisk</span></span>

## <span data-ttu-id="d8952-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8952-102">SYNOPSIS</span></span>
<span data-ttu-id="d8952-103">Erstellt einen verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="d8952-103">Creates a managed disk.</span></span>

## <span data-ttu-id="d8952-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8952-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8952-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8952-105">DESCRIPTION</span></span>
<span data-ttu-id="d8952-106">Das Cmdlet **New-AzDisk** erstellt einen verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="d8952-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="d8952-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8952-107">EXAMPLES</span></span>

### <span data-ttu-id="d8952-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8952-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="d8952-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="d8952-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="d8952-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d8952-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d8952-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="d8952-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="d8952-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d8952-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d8952-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8952-113">PARAMETERS</span></span>

### <span data-ttu-id="d8952-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8952-114">-AsJob</span></span>
<span data-ttu-id="d8952-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="d8952-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8952-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8952-116">-DefaultProfile</span></span>
<span data-ttu-id="d8952-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8952-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8952-118">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="d8952-118">-Disk</span></span>
<span data-ttu-id="d8952-119">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="d8952-119">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8952-120">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="d8952-120">-DiskName</span></span>
<span data-ttu-id="d8952-121">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d8952-121">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8952-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8952-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8952-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d8952-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8952-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8952-124">-Confirm</span></span>
<span data-ttu-id="d8952-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8952-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8952-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8952-126">-WhatIf</span></span>
<span data-ttu-id="d8952-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8952-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8952-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8952-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8952-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8952-129">CommonParameters</span></span>
<span data-ttu-id="d8952-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8952-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8952-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8952-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8952-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8952-132">INPUTS</span></span>

### <span data-ttu-id="d8952-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d8952-133">System.String</span></span>
<span data-ttu-id="d8952-134">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="d8952-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="d8952-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8952-135">OUTPUTS</span></span>

### <span data-ttu-id="d8952-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="d8952-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="d8952-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8952-137">NOTES</span></span>

## <span data-ttu-id="d8952-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8952-138">RELATED LINKS</span></span>

