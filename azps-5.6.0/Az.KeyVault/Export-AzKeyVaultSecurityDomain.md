---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 6373ddf37e95c8451afbe8a24b6bade2ca5d3bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940432"
---
# <span data-ttu-id="0867d-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="0867d-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="0867d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0867d-102">SYNOPSIS</span></span>
<span data-ttu-id="0867d-103">Exportiert die Sicherheitsdomänendaten eines verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="0867d-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="0867d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0867d-104">SYNTAX</span></span>

### <span data-ttu-id="0867d-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0867d-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0867d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0867d-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0867d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0867d-107">DESCRIPTION</span></span>
<span data-ttu-id="0867d-108">Exportiert die Sicherheitsdomänendaten eines verwalteten HSM zum Importieren in ein anderes HSM.</span><span class="sxs-lookup"><span data-stu-id="0867d-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="0867d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0867d-109">EXAMPLES</span></span>

### <span data-ttu-id="0867d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0867d-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="0867d-111">Dieser Befehl ruft das verwaltete HSM namens testmhsm ab und speichert eine Sicherung dieser verwalteten HSM-Sicherheitsdomäne in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="0867d-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="0867d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0867d-112">PARAMETERS</span></span>

### <span data-ttu-id="0867d-113">-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="0867d-113">-Certificates</span></span>
<span data-ttu-id="0867d-114">Pfade zu den Zertifikaten, die zum Verschlüsseln der Sicherheitsdomänendaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0867d-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

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

### <span data-ttu-id="0867d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0867d-115">-DefaultProfile</span></span>
<span data-ttu-id="0867d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0867d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0867d-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0867d-117">-Force</span></span>
<span data-ttu-id="0867d-118">Geben Sie an, ob vorhandene Datei überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0867d-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="0867d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0867d-119">-InputObject</span></span>
<span data-ttu-id="0867d-120">Objekt, das einen verwalteten HSM darstellt.</span><span class="sxs-lookup"><span data-stu-id="0867d-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="0867d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0867d-121">-Name</span></span>
<span data-ttu-id="0867d-122">Name des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="0867d-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="0867d-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="0867d-123">-OutputPath</span></span>
<span data-ttu-id="0867d-124">Geben Sie den Pfad an, in den Sicherheitsdomänendaten heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0867d-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="0867d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0867d-125">-PassThru</span></span>
<span data-ttu-id="0867d-126">Wenn angegeben wird, wird ein boolescher Wert zurückgegeben, wenn das Cmdlet erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0867d-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="0867d-127">-Quorum</span><span class="sxs-lookup"><span data-stu-id="0867d-127">-Quorum</span></span>
<span data-ttu-id="0867d-128">Die Mindestanzahl von Freigaben, die zum Entschlüsseln der Sicherheitsdomäne für die Wiederherstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0867d-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

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

### <span data-ttu-id="0867d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0867d-129">-Confirm</span></span>
<span data-ttu-id="0867d-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0867d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0867d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0867d-131">-WhatIf</span></span>
<span data-ttu-id="0867d-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0867d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0867d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0867d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0867d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0867d-134">CommonParameters</span></span>
<span data-ttu-id="0867d-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0867d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0867d-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0867d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0867d-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0867d-137">INPUTS</span></span>

### <span data-ttu-id="0867d-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0867d-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="0867d-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0867d-139">OUTPUTS</span></span>

### <span data-ttu-id="0867d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0867d-140">System.Boolean</span></span>

## <span data-ttu-id="0867d-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0867d-141">NOTES</span></span>

## <span data-ttu-id="0867d-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0867d-142">RELATED LINKS</span></span>
