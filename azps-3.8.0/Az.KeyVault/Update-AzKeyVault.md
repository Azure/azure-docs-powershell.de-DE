---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846024"
---
# <span data-ttu-id="97db3-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="97db3-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="97db3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97db3-102">SYNOPSIS</span></span>
<span data-ttu-id="97db3-103">Aktualisieren Sie den Zustand eines Azure Key Vaults.</span><span class="sxs-lookup"><span data-stu-id="97db3-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="97db3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97db3-104">SYNTAX</span></span>

### <span data-ttu-id="97db3-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="97db3-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97db3-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97db3-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97db3-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97db3-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97db3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97db3-108">DESCRIPTION</span></span>
<span data-ttu-id="97db3-109">Dieses Cmdlet aktualisiert den Zustand eines Azure Key Vaults.</span><span class="sxs-lookup"><span data-stu-id="97db3-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="97db3-110">Bitte beachten Sie, dass die Aktualisierung einiger Eigenschaften eine irreversible Aktion ist, beispielsweise wenn die Option "Soft Delete" aktiviert ist, kann Sie nicht mehr deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="97db3-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="97db3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97db3-111">EXAMPLES</span></span>

### <span data-ttu-id="97db3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97db3-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="97db3-113">Aktiviert die Soft-Delete-Funktion im schlüsseltresor `$keyVaultName` , der in der Ressourcengruppe benannt ist `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="97db3-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="97db3-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="97db3-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="97db3-115">Aktiviert den Bereinigungs Schutz mithilfe der Rohrleitungs Syntax.</span><span class="sxs-lookup"><span data-stu-id="97db3-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="97db3-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="97db3-116">PARAMETERS</span></span>

### <span data-ttu-id="97db3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97db3-117">-DefaultProfile</span></span>
<span data-ttu-id="97db3-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97db3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db3-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="97db3-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="97db3-120">Aktivieren Sie die Funktion zum Bereinigen von Schutz für diesen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="97db3-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="97db3-121">Sobald die Funktion aktiviert ist, kann Sie nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="97db3-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="97db3-122">Es muss Soft-Delete aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="97db3-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="97db3-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="97db3-123">-EnableSoftDelete</span></span>
<span data-ttu-id="97db3-124">Aktivieren Sie die Soft-Delete-Funktion für diesen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="97db3-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="97db3-125">Sobald die Funktion aktiviert ist, kann Sie nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="97db3-125">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="97db3-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="97db3-126">-InputObject</span></span>
<span data-ttu-id="97db3-127">Vault-Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="97db3-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97db3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97db3-128">-ResourceGroupName</span></span>
<span data-ttu-id="97db3-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="97db3-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db3-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="97db3-130">-ResourceId</span></span>
<span data-ttu-id="97db3-131">Ressourcen-ID des Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="97db3-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97db3-132">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="97db3-132">-VaultName</span></span>
<span data-ttu-id="97db3-133">Name des Schlüsselspeichers</span><span class="sxs-lookup"><span data-stu-id="97db3-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db3-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="97db3-134">-Confirm</span></span>
<span data-ttu-id="97db3-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97db3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97db3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97db3-136">-WhatIf</span></span>
<span data-ttu-id="97db3-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97db3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97db3-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97db3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97db3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97db3-139">CommonParameters</span></span>
<span data-ttu-id="97db3-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97db3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97db3-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97db3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97db3-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97db3-142">INPUTS</span></span>

### <span data-ttu-id="97db3-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="97db3-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="97db3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="97db3-144">System.String</span></span>

## <span data-ttu-id="97db3-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97db3-145">OUTPUTS</span></span>

### <span data-ttu-id="97db3-146">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="97db3-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="97db3-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="97db3-147">NOTES</span></span>

## <span data-ttu-id="97db3-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97db3-148">RELATED LINKS</span></span>
