---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175236"
---
# <span data-ttu-id="bff3a-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="bff3a-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="bff3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bff3a-103">Importiert zuvor exportierte Sicherheitsdomänendaten in ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="bff3a-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="bff3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bff3a-104">SYNTAX</span></span>

### <span data-ttu-id="bff3a-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bff3a-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bff3a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bff3a-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bff3a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bff3a-107">DESCRIPTION</span></span>
<span data-ttu-id="bff3a-108">Dieses Cmdlet importiert zuvor exportierte Sicherheitsdomänendaten in ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="bff3a-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="bff3a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bff3a-109">EXAMPLES</span></span>

### <span data-ttu-id="bff3a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bff3a-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="bff3a-111">Zuerst müssen die Schlüssel bereitgestellt werden, um die Daten der Sicherheitsdomäne zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="bff3a-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="bff3a-112">Anschließend stellt der **Befehl "Import-AzKeyVaultSecurityDomain"** zuvor gesicherte Sicherheitsdomänendaten mithilfe dieser Schlüssel auf einem verwalteten HSM wieder zurück.</span><span class="sxs-lookup"><span data-stu-id="bff3a-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="bff3a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bff3a-113">PARAMETERS</span></span>

### <span data-ttu-id="bff3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff3a-114">-DefaultProfile</span></span>
<span data-ttu-id="bff3a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bff3a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff3a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bff3a-116">-InputObject</span></span>
<span data-ttu-id="bff3a-117">Objekt, das einen verwalteten HSM darstellt.</span><span class="sxs-lookup"><span data-stu-id="bff3a-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bff3a-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="bff3a-118">-Keys</span></span>
<span data-ttu-id="bff3a-119">Informationen zu den Schlüsseln, die zum Entschlüsseln der Daten der Sicherheitsdomäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bff3a-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="bff3a-120">Sehen Sie sich Beispiele für deren Bau an.</span><span class="sxs-lookup"><span data-stu-id="bff3a-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff3a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bff3a-121">-Name</span></span>
<span data-ttu-id="bff3a-122">Name des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="bff3a-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff3a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bff3a-123">-PassThru</span></span>
<span data-ttu-id="bff3a-124">Bei Angabe wird ein boolescher Wert zurückgegeben, wenn das Cmdlet erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="bff3a-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="bff3a-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="bff3a-125">-SecurityDomainPath</span></span>
<span data-ttu-id="bff3a-126">Geben Sie den Pfad zu den verschlüsselten Sicherheitsdomänendaten an.</span><span class="sxs-lookup"><span data-stu-id="bff3a-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff3a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bff3a-127">-Confirm</span></span>
<span data-ttu-id="bff3a-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bff3a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff3a-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bff3a-129">-WhatIf</span></span>
<span data-ttu-id="bff3a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bff3a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff3a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bff3a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff3a-132">CommonParameters</span></span>
<span data-ttu-id="bff3a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff3a-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bff3a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff3a-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bff3a-135">INPUTS</span></span>

### <span data-ttu-id="bff3a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bff3a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="bff3a-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bff3a-137">OUTPUTS</span></span>

### <span data-ttu-id="bff3a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bff3a-138">System.Boolean</span></span>

## <span data-ttu-id="bff3a-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bff3a-139">NOTES</span></span>

## <span data-ttu-id="bff3a-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bff3a-140">RELATED LINKS</span></span>
