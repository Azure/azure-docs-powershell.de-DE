---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009346"
---
# <span data-ttu-id="72ea9-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="72ea9-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="72ea9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="72ea9-103">Erstellt ein konfigurierbares Festplatten-Verschlüsselungs Satz Objekt.</span><span class="sxs-lookup"><span data-stu-id="72ea9-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="72ea9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72ea9-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ea9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="72ea9-106">Erstellt ein konfigurierbares Festplatten-Verschlüsselungs Satz Objekt.</span><span class="sxs-lookup"><span data-stu-id="72ea9-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="72ea9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72ea9-107">EXAMPLES</span></span>

### <span data-ttu-id="72ea9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72ea9-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="72ea9-109">Erstellt den Festplatten-Verschlüsselungs Satz mit dem angegebenen aktiven Schlüssel im Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="72ea9-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="72ea9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="72ea9-110">PARAMETERS</span></span>

### <span data-ttu-id="72ea9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ea9-111">-DefaultProfile</span></span>
<span data-ttu-id="72ea9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72ea9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72ea9-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="72ea9-113">-EncryptionType</span></span>
<span data-ttu-id="72ea9-114">Verwenden Sie diese Einstellung, um den Verschlüsselungstyp des Datenträger Verschlüsselungs Satzes festzulegen.</span><span class="sxs-lookup"><span data-stu-id="72ea9-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="72ea9-115">Die verfügbaren Werte lauten: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey".</span><span class="sxs-lookup"><span data-stu-id="72ea9-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ea9-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="72ea9-116">-IdentityType</span></span>
<span data-ttu-id="72ea9-117">Der Typ der verwalteten Identität, die von der DiskEncryptionSet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72ea9-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="72ea9-118">Nur SystemAssigned wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72ea9-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="72ea9-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="72ea9-119">-KeyUrl</span></span>
<span data-ttu-id="72ea9-120">URL, der auf den aktiven Schlüssel in keyvault zeigt</span><span class="sxs-lookup"><span data-stu-id="72ea9-120">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ea9-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="72ea9-121">-Location</span></span>
<span data-ttu-id="72ea9-122">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="72ea9-122">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ea9-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="72ea9-123">-SourceVaultId</span></span>
<span data-ttu-id="72ea9-124">Die Ressourcen-ID des keyvaults mit dem aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="72ea9-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ea9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="72ea9-125">-Tag</span></span>
<span data-ttu-id="72ea9-126">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="72ea9-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="72ea9-127">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="72ea9-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ea9-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72ea9-128">-Confirm</span></span>
<span data-ttu-id="72ea9-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72ea9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ea9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ea9-130">-WhatIf</span></span>
<span data-ttu-id="72ea9-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72ea9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72ea9-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72ea9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ea9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ea9-133">CommonParameters</span></span>
<span data-ttu-id="72ea9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ea9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ea9-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72ea9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ea9-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72ea9-136">INPUTS</span></span>

### <span data-ttu-id="72ea9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="72ea9-137">System.String</span></span>

### <span data-ttu-id="72ea9-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="72ea9-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="72ea9-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72ea9-139">OUTPUTS</span></span>

### <span data-ttu-id="72ea9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="72ea9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="72ea9-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="72ea9-141">NOTES</span></span>

## <span data-ttu-id="72ea9-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72ea9-142">RELATED LINKS</span></span>
