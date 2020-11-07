---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 4392c1ccf19474e1a8f73c5bccca2c09f53cbea8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665267"
---
# <span data-ttu-id="655c4-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="655c4-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="655c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="655c4-102">SYNOPSIS</span></span>
<span data-ttu-id="655c4-103">Erstellt einen verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="655c4-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="655c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="655c4-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="655c4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="655c4-105">DESCRIPTION</span></span>
<span data-ttu-id="655c4-106">Das Cmdlet **New-AzureRmDisk** erstellt einen verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="655c4-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="655c4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="655c4-107">EXAMPLES</span></span>

### <span data-ttu-id="655c4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="655c4-108">Example 1</span></span>
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

<span data-ttu-id="655c4-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="655c4-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="655c4-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="655c4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="655c4-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="655c4-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="655c4-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="655c4-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="655c4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="655c4-113">PARAMETERS</span></span>

### <span data-ttu-id="655c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="655c4-114">-DefaultProfile</span></span>
<span data-ttu-id="655c4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="655c4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="655c4-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="655c4-116">-Disk</span></span>
<span data-ttu-id="655c4-117">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="655c4-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="655c4-118">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="655c4-118">-DiskName</span></span>
<span data-ttu-id="655c4-119">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="655c4-119">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="655c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="655c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="655c4-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="655c4-121">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="655c4-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="655c4-122">-Confirm</span></span>
<span data-ttu-id="655c4-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="655c4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="655c4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="655c4-124">-WhatIf</span></span>
<span data-ttu-id="655c4-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="655c4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="655c4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="655c4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="655c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="655c4-127">CommonParameters</span></span>
<span data-ttu-id="655c4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="655c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="655c4-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="655c4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="655c4-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="655c4-130">INPUTS</span></span>

### <span data-ttu-id="655c4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="655c4-131">System.String</span></span>
<span data-ttu-id="655c4-132">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="655c4-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="655c4-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="655c4-133">OUTPUTS</span></span>

### <span data-ttu-id="655c4-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="655c4-134">System.Object</span></span>

## <span data-ttu-id="655c4-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="655c4-135">NOTES</span></span>

## <span data-ttu-id="655c4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="655c4-136">RELATED LINKS</span></span>

