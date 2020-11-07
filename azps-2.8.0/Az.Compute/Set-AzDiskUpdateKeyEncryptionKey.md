---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 5a6ea0eede8c7e9f6311c5d951f8e19176f532c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651949"
---
# <span data-ttu-id="84dc3-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="84dc3-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="84dc3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="84dc3-103">Legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="84dc3-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="84dc3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84dc3-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84dc3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="84dc3-106">Das Cmdlet " **Set-AzDiskUpdateKeyEncryptionKey** " legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="84dc3-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="84dc3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="84dc3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84dc3-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="84dc3-109">Der erste Befehl erstellt ein lokales leeres Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="84dc3-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="84dc3-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="84dc3-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="84dc3-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="84dc3-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="84dc3-112">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="84dc3-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="84dc3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="84dc3-113">PARAMETERS</span></span>

### <span data-ttu-id="84dc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84dc3-114">-DefaultProfile</span></span>
<span data-ttu-id="84dc3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84dc3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84dc3-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="84dc3-116">-DiskUpdate</span></span>
<span data-ttu-id="84dc3-117">Gibt ein lokales Datenträger Aktualisierungs Objekt an.</span><span class="sxs-lookup"><span data-stu-id="84dc3-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84dc3-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="84dc3-118">-KeyUrl</span></span>
<span data-ttu-id="84dc3-119">Gibt die Schlüssel-URL an.</span><span class="sxs-lookup"><span data-stu-id="84dc3-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="84dc3-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="84dc3-120">-SourceVaultId</span></span>
<span data-ttu-id="84dc3-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="84dc3-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="84dc3-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84dc3-122">-Confirm</span></span>
<span data-ttu-id="84dc3-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84dc3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84dc3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84dc3-124">-WhatIf</span></span>
<span data-ttu-id="84dc3-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84dc3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84dc3-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84dc3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84dc3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84dc3-127">CommonParameters</span></span>
<span data-ttu-id="84dc3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84dc3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84dc3-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84dc3-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84dc3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84dc3-130">INPUTS</span></span>

### <span data-ttu-id="84dc3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="84dc3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="84dc3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="84dc3-132">System.String</span></span>

## <span data-ttu-id="84dc3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84dc3-133">OUTPUTS</span></span>

### <span data-ttu-id="84dc3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="84dc3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="84dc3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="84dc3-135">NOTES</span></span>

## <span data-ttu-id="84dc3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84dc3-136">RELATED LINKS</span></span>
