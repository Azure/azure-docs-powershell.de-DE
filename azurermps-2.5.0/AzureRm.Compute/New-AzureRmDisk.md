---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 2cb1cad343f57f164529e3607c1ad0b1ec74df05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848527"
---
# <span data-ttu-id="a6c21-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a6c21-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="a6c21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6c21-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c21-103">Erstellt einen verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a6c21-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6c21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6c21-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6c21-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c21-106">Das Cmdlet **New-AzureRmDisk** erstellt einen verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a6c21-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="a6c21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6c21-107">EXAMPLES</span></span>

### <span data-ttu-id="a6c21-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6c21-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="a6c21-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="a6c21-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="a6c21-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6c21-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a6c21-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="a6c21-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="a6c21-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a6c21-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a6c21-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6c21-113">PARAMETERS</span></span>

### <span data-ttu-id="a6c21-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6c21-114">-AsJob</span></span>
<span data-ttu-id="a6c21-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="a6c21-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6c21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c21-116">-DefaultProfile</span></span>
<span data-ttu-id="a6c21-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6c21-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6c21-118">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="a6c21-118">-Disk</span></span>
<span data-ttu-id="a6c21-119">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="a6c21-119">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="a6c21-120">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="a6c21-120">-DiskName</span></span>
<span data-ttu-id="a6c21-121">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a6c21-121">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="a6c21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c21-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6c21-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a6c21-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a6c21-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6c21-124">-Confirm</span></span>
<span data-ttu-id="a6c21-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6c21-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c21-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c21-126">-WhatIf</span></span>
<span data-ttu-id="a6c21-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6c21-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c21-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6c21-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c21-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c21-129">CommonParameters</span></span>
<span data-ttu-id="a6c21-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c21-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c21-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c21-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c21-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6c21-132">INPUTS</span></span>

### <span data-ttu-id="a6c21-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a6c21-133">System.String</span></span>
<span data-ttu-id="a6c21-134">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="a6c21-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="a6c21-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6c21-135">OUTPUTS</span></span>

### <span data-ttu-id="a6c21-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="a6c21-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="a6c21-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6c21-137">NOTES</span></span>

## <span data-ttu-id="a6c21-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6c21-138">RELATED LINKS</span></span>

