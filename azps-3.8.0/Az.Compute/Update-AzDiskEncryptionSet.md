---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004795"
---
# <span data-ttu-id="1e9ce-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1e9ce-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="1e9ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9ce-103">Aktualisiert einen Datenträger Verschlüsselungs Satz.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="1e9ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e9ce-104">SYNTAX</span></span>

### <span data-ttu-id="1e9ce-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e9ce-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9ce-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1e9ce-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e9ce-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1e9ce-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e9ce-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e9ce-108">DESCRIPTION</span></span>
<span data-ttu-id="1e9ce-109">Aktualisiert einen Datenträger Verschlüsselungs Satz.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="1e9ce-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e9ce-110">EXAMPLES</span></span>

### <span data-ttu-id="1e9ce-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e9ce-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="1e9ce-112">Aktualisiert den Datenträger Verschlüsselungs Satz mithilfe des angegebenen aktiven Schlüssels im Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="1e9ce-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e9ce-113">PARAMETERS</span></span>

### <span data-ttu-id="1e9ce-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e9ce-114">-AsJob</span></span>
<span data-ttu-id="1e9ce-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1e9ce-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9ce-116">-DefaultProfile</span></span>
<span data-ttu-id="1e9ce-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e9ce-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1e9ce-118">-InputObject</span></span>
<span data-ttu-id="1e9ce-119">Das lokale Objekt des Datenträger Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9ce-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="1e9ce-120">-KeyUrl</span></span>
<span data-ttu-id="1e9ce-121">URL, der auf den aktiven Schlüssel in keyvault zeigt</span><span class="sxs-lookup"><span data-stu-id="1e9ce-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="1e9ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1e9ce-122">-Name</span></span>
<span data-ttu-id="1e9ce-123">Name des Festplatten-Verschlüsselungs Satzes.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e9ce-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9ce-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1e9ce-126">-ResourceId</span></span>
<span data-ttu-id="1e9ce-127">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e9ce-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1e9ce-128">-SourceVaultId</span></span>
<span data-ttu-id="1e9ce-129">Die Ressourcen-ID des keyvaults mit dem aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="1e9ce-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e9ce-130">-Tag</span></span>
<span data-ttu-id="1e9ce-131">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="1e9ce-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1e9ce-132">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="1e9ce-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1e9ce-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e9ce-133">-Confirm</span></span>
<span data-ttu-id="1e9ce-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9ce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9ce-135">-WhatIf</span></span>
<span data-ttu-id="1e9ce-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e9ce-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9ce-138">CommonParameters</span></span>
<span data-ttu-id="1e9ce-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e9ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9ce-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e9ce-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9ce-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e9ce-141">INPUTS</span></span>

### <span data-ttu-id="1e9ce-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1e9ce-142">System.String</span></span>

### <span data-ttu-id="1e9ce-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1e9ce-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="1e9ce-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e9ce-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1e9ce-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e9ce-145">OUTPUTS</span></span>

### <span data-ttu-id="1e9ce-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1e9ce-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="1e9ce-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e9ce-147">NOTES</span></span>

## <span data-ttu-id="1e9ce-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e9ce-148">RELATED LINKS</span></span>
