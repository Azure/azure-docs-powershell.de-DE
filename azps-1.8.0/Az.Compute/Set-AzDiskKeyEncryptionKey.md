---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: fa3a1df514793b64158190c652211904db59ab9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820571"
---
# <span data-ttu-id="54871-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="54871-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="54871-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54871-102">SYNOPSIS</span></span>
<span data-ttu-id="54871-103">Legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="54871-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="54871-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54871-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54871-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54871-105">DESCRIPTION</span></span>
<span data-ttu-id="54871-106">Das Cmdlet " **Set-AzDiskKeyEncryptionKey** " legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="54871-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="54871-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54871-107">EXAMPLES</span></span>

### <span data-ttu-id="54871-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54871-108">Example 1</span></span>
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

<span data-ttu-id="54871-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="54871-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="54871-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="54871-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="54871-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="54871-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="54871-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="54871-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="54871-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="54871-113">PARAMETERS</span></span>

### <span data-ttu-id="54871-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54871-114">-DefaultProfile</span></span>
<span data-ttu-id="54871-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54871-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54871-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="54871-116">-Disk</span></span>
<span data-ttu-id="54871-117">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="54871-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54871-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="54871-118">-KeyUrl</span></span>
<span data-ttu-id="54871-119">Gibt an die Schlüssel-URL.</span><span class="sxs-lookup"><span data-stu-id="54871-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="54871-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="54871-120">-SourceVaultId</span></span>
<span data-ttu-id="54871-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="54871-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="54871-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54871-122">-Confirm</span></span>
<span data-ttu-id="54871-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54871-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54871-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54871-124">-WhatIf</span></span>
<span data-ttu-id="54871-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54871-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54871-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54871-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54871-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54871-127">CommonParameters</span></span>
<span data-ttu-id="54871-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54871-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54871-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54871-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54871-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54871-130">INPUTS</span></span>

### <span data-ttu-id="54871-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="54871-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="54871-132">System. String</span><span class="sxs-lookup"><span data-stu-id="54871-132">System.String</span></span>

## <span data-ttu-id="54871-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54871-133">OUTPUTS</span></span>

### <span data-ttu-id="54871-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="54871-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="54871-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="54871-135">NOTES</span></span>

## <span data-ttu-id="54871-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54871-136">RELATED LINKS</span></span>
