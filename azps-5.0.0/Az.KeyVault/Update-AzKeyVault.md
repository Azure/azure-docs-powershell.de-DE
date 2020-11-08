---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175482"
---
# <span data-ttu-id="afff4-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="afff4-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="afff4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afff4-102">SYNOPSIS</span></span>
<span data-ttu-id="afff4-103">Aktualisieren Sie den Zustand eines Azure Key Vaults.</span><span class="sxs-lookup"><span data-stu-id="afff4-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="afff4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afff4-104">SYNTAX</span></span>

### <span data-ttu-id="afff4-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="afff4-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afff4-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afff4-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afff4-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afff4-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afff4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afff4-108">DESCRIPTION</span></span>
<span data-ttu-id="afff4-109">Dieses Cmdlet aktualisiert den Zustand eines Azure Key Vaults.</span><span class="sxs-lookup"><span data-stu-id="afff4-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="afff4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afff4-110">EXAMPLES</span></span>

### <span data-ttu-id="afff4-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="afff4-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="afff4-112">Aktiviert den Bereinigungs Schutz mithilfe der Rohrleitungs Syntax.</span><span class="sxs-lookup"><span data-stu-id="afff4-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="afff4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="afff4-113">PARAMETERS</span></span>

### <span data-ttu-id="afff4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afff4-114">-DefaultProfile</span></span>
<span data-ttu-id="afff4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="afff4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afff4-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="afff4-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="afff4-117">Aktivieren Sie die Funktion zum Bereinigen von Schutz für diesen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="afff4-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="afff4-118">Sobald die Funktion aktiviert ist, kann Sie nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="afff4-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="afff4-119">Es muss Soft-Delete aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="afff4-119">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="afff4-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="afff4-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="afff4-121">Aktivieren oder deaktivieren Sie diesen schlüsseltresor, um Daten Aktionen nach rollenbasierter Zugriffssteuerung zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="afff4-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afff4-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="afff4-122">-InputObject</span></span>
<span data-ttu-id="afff4-123">Vault-Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="afff4-123">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afff4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afff4-124">-ResourceGroupName</span></span>
<span data-ttu-id="afff4-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="afff4-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afff4-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="afff4-126">-ResourceId</span></span>
<span data-ttu-id="afff4-127">Ressourcen-ID des Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="afff4-127">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afff4-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="afff4-128">-VaultName</span></span>
<span data-ttu-id="afff4-129">Name des Schlüsselspeichers</span><span class="sxs-lookup"><span data-stu-id="afff4-129">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afff4-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afff4-130">-Confirm</span></span>
<span data-ttu-id="afff4-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afff4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afff4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afff4-132">-WhatIf</span></span>
<span data-ttu-id="afff4-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afff4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afff4-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afff4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afff4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afff4-135">CommonParameters</span></span>
<span data-ttu-id="afff4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afff4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afff4-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afff4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afff4-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afff4-138">INPUTS</span></span>

### <span data-ttu-id="afff4-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="afff4-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="afff4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="afff4-140">System.String</span></span>

## <span data-ttu-id="afff4-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afff4-141">OUTPUTS</span></span>

### <span data-ttu-id="afff4-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="afff4-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="afff4-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="afff4-143">NOTES</span></span>

## <span data-ttu-id="afff4-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afff4-144">RELATED LINKS</span></span>
