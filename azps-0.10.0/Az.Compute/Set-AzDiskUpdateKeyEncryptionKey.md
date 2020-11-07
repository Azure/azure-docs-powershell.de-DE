---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: b1fe2674360ffec8b2f2c570d47aef3daad78e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844283"
---
# <span data-ttu-id="fae43-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fae43-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="fae43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fae43-102">SYNOPSIS</span></span>
<span data-ttu-id="fae43-103">Legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="fae43-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="fae43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fae43-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fae43-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fae43-105">DESCRIPTION</span></span>
<span data-ttu-id="fae43-106">Das Cmdlet " **Set-AzDiskUpdateKeyEncryptionKey** " legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="fae43-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="fae43-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fae43-107">EXAMPLES</span></span>

### <span data-ttu-id="fae43-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fae43-108">Example 1</span></span>
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

<span data-ttu-id="fae43-109">Der erste Befehl erstellt ein lokales leeres Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="fae43-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="fae43-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fae43-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="fae43-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="fae43-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="fae43-112">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fae43-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fae43-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fae43-113">PARAMETERS</span></span>

### <span data-ttu-id="fae43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae43-114">-DefaultProfile</span></span>
<span data-ttu-id="fae43-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fae43-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae43-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="fae43-116">-DiskUpdate</span></span>
<span data-ttu-id="fae43-117">Gibt ein lokales Datenträger Aktualisierungs Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fae43-117">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fae43-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="fae43-118">-KeyUrl</span></span>
<span data-ttu-id="fae43-119">Gibt an die Schlüssel-URL.</span><span class="sxs-lookup"><span data-stu-id="fae43-119">Specifes the key Url.</span></span>

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

### <span data-ttu-id="fae43-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="fae43-120">-SourceVaultId</span></span>
<span data-ttu-id="fae43-121">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="fae43-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="fae43-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fae43-122">-Confirm</span></span>
<span data-ttu-id="fae43-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fae43-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae43-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae43-124">-WhatIf</span></span>
<span data-ttu-id="fae43-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fae43-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fae43-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fae43-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae43-127">CommonParameters</span></span>
<span data-ttu-id="fae43-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae43-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae43-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae43-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fae43-130">INPUTS</span></span>

### <span data-ttu-id="fae43-131">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="fae43-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="fae43-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fae43-132">System.String</span></span>

## <span data-ttu-id="fae43-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fae43-133">OUTPUTS</span></span>

### <span data-ttu-id="fae43-134">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="fae43-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="fae43-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fae43-135">NOTES</span></span>

## <span data-ttu-id="fae43-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fae43-136">RELATED LINKS</span></span>

