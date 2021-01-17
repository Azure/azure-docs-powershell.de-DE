---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469587"
---
# <span data-ttu-id="83fb8-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="83fb8-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="83fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="83fb8-103">Exportiert die Sicherheitsdomänendaten eines verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="83fb8-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="83fb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83fb8-104">SYNTAX</span></span>

### <span data-ttu-id="83fb8-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="83fb8-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83fb8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83fb8-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83fb8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83fb8-107">DESCRIPTION</span></span>
<span data-ttu-id="83fb8-108">Exportiert die Sicherheitsdomänendaten eines verwalteten HSM für den Import auf einem anderen HSM.</span><span class="sxs-lookup"><span data-stu-id="83fb8-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="83fb8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83fb8-109">EXAMPLES</span></span>

### <span data-ttu-id="83fb8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83fb8-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="83fb8-111">Dieser Befehl ruft den verwalteten HSM-benannten Testmhsm ab und speichert eine Sicherung dieser verwalteten HSM-Sicherheitsdomäne in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="83fb8-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="83fb8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83fb8-112">PARAMETERS</span></span>

### <span data-ttu-id="83fb8-113">-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="83fb8-113">-Certificates</span></span>
<span data-ttu-id="83fb8-114">Pfade zu den Zertifikaten, die zum Verschlüsseln der Daten der Sicherheitsdomäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83fb8-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fb8-115">-DefaultProfile</span></span>
<span data-ttu-id="83fb8-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83fb8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83fb8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="83fb8-117">-Force</span></span>
<span data-ttu-id="83fb8-118">Geben Sie an, ob eine vorhandene Datei überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="83fb8-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="83fb8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83fb8-119">-InputObject</span></span>
<span data-ttu-id="83fb8-120">Objekt, das einen verwalteten HSM darstellt.</span><span class="sxs-lookup"><span data-stu-id="83fb8-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="83fb8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="83fb8-121">-Name</span></span>
<span data-ttu-id="83fb8-122">Name des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="83fb8-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="83fb8-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="83fb8-123">-OutputPath</span></span>
<span data-ttu-id="83fb8-124">Geben Sie den Pfad an, auf den Sicherheitsdomänendaten heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="83fb8-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fb8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83fb8-125">-PassThru</span></span>
<span data-ttu-id="83fb8-126">Bei Angabe wird ein boolescher Wert zurückgegeben, wenn das Cmdlet erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="83fb8-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="83fb8-127">-Umg.</span><span class="sxs-lookup"><span data-stu-id="83fb8-127">-Quorum</span></span>
<span data-ttu-id="83fb8-128">Die Mindestanzahl von Freigaben, die zum Entschlüsseln der Sicherheitsdomäne für die Wiederherstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="83fb8-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fb8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83fb8-129">-Confirm</span></span>
<span data-ttu-id="83fb8-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83fb8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83fb8-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="83fb8-131">-WhatIf</span></span>
<span data-ttu-id="83fb8-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83fb8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83fb8-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83fb8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83fb8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fb8-134">CommonParameters</span></span>
<span data-ttu-id="83fb8-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83fb8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fb8-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83fb8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fb8-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83fb8-137">INPUTS</span></span>

### <span data-ttu-id="83fb8-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="83fb8-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="83fb8-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83fb8-139">OUTPUTS</span></span>

### <span data-ttu-id="83fb8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83fb8-140">System.Boolean</span></span>

## <span data-ttu-id="83fb8-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="83fb8-141">NOTES</span></span>

## <span data-ttu-id="83fb8-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="83fb8-142">RELATED LINKS</span></span>
