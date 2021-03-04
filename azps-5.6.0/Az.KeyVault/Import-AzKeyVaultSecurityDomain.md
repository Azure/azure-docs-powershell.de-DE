---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 3175685478afada44e8870e772a56ce91992bbc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944111"
---
# <span data-ttu-id="01da5-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="01da5-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="01da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01da5-102">SYNOPSIS</span></span>
<span data-ttu-id="01da5-103">Importiert zuvor exportierte Sicherheitsdomänendaten in ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="01da5-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="01da5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01da5-104">SYNTAX</span></span>

### <span data-ttu-id="01da5-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="01da5-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01da5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="01da5-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01da5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01da5-107">DESCRIPTION</span></span>
<span data-ttu-id="01da5-108">Dieses Cmdlet importiert zuvor exportierte Sicherheitsdomänendaten in ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="01da5-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="01da5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01da5-109">EXAMPLES</span></span>

### <span data-ttu-id="01da5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01da5-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="01da5-111">Zuerst müssen die Schlüssel bereitgestellt werden, um die Daten der Sicherheitsdomäne zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="01da5-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="01da5-112">Anschließend werden mit dem **Befehl Import-AzKeyVaultSecurityDomain** zuvor gesicherte Sicherheitsdomänendaten mithilfe dieser Schlüssel in einem verwalteten HSM wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="01da5-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="01da5-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="01da5-113">PARAMETERS</span></span>

### <span data-ttu-id="01da5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01da5-114">-DefaultProfile</span></span>
<span data-ttu-id="01da5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01da5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01da5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01da5-116">-InputObject</span></span>
<span data-ttu-id="01da5-117">Objekt, das einen verwalteten HSM darstellt.</span><span class="sxs-lookup"><span data-stu-id="01da5-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="01da5-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="01da5-118">-Keys</span></span>
<span data-ttu-id="01da5-119">Informationen zu den Schlüsseln, die zum Entschlüsseln der Sicherheitsdomänendaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01da5-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="01da5-120">Hier finden Sie Beispiele für die Art und Weise, wie sie erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="01da5-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="01da5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="01da5-121">-Name</span></span>
<span data-ttu-id="01da5-122">Name des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="01da5-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="01da5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01da5-123">-PassThru</span></span>
<span data-ttu-id="01da5-124">Wenn angegeben wird, wird ein boolescher Wert zurückgegeben, wenn das Cmdlet erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01da5-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="01da5-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="01da5-125">-SecurityDomainPath</span></span>
<span data-ttu-id="01da5-126">Geben Sie den Pfad zu den verschlüsselten Sicherheitsdomänendaten an.</span><span class="sxs-lookup"><span data-stu-id="01da5-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="01da5-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01da5-127">-Confirm</span></span>
<span data-ttu-id="01da5-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01da5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01da5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01da5-129">-WhatIf</span></span>
<span data-ttu-id="01da5-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01da5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01da5-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01da5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01da5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01da5-132">CommonParameters</span></span>
<span data-ttu-id="01da5-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01da5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01da5-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01da5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01da5-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01da5-135">INPUTS</span></span>

### <span data-ttu-id="01da5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="01da5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="01da5-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01da5-137">OUTPUTS</span></span>

### <span data-ttu-id="01da5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01da5-138">System.Boolean</span></span>

## <span data-ttu-id="01da5-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="01da5-139">NOTES</span></span>

## <span data-ttu-id="01da5-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="01da5-140">RELATED LINKS</span></span>
