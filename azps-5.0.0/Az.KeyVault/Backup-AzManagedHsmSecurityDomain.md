---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: 10a54afa8a6ef2e37beebd9d6cdcd304b2d13979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296871"
---
# <span data-ttu-id="ca3f3-101">Backup-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="ca3f3-101">Backup-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="ca3f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3f3-103">Sichern Sie die Sicherheitsdomänen Daten eines verwalteten HSM zur Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-103">Backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="ca3f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca3f3-104">SYNTAX</span></span>

### <span data-ttu-id="ca3f3-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca3f3-105">ByName (Default)</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca3f3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ca3f3-106">ByInputObject</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca3f3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca3f3-107">DESCRIPTION</span></span>
<span data-ttu-id="ca3f3-108">Mit diesem Cmdlet werden die Sicherheitsdomänen Daten eines verwalteten HSM zur Wiederherstellung gesichert.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-108">This cmdlet backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="ca3f3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca3f3-109">EXAMPLES</span></span>

### <span data-ttu-id="ca3f3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca3f3-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="ca3f3-111">Dieser Befehl ruft das verwaltete HSM mit dem Namen testmhsm ab und speichert eine Sicherungskopie dieser verwalteten HSM-Sicherheitsdomäne in der angegebenen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="ca3f3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca3f3-112">PARAMETERS</span></span>

### <span data-ttu-id="ca3f3-113">-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="ca3f3-113">-Certificates</span></span>
<span data-ttu-id="ca3f3-114">Pfade zu den Zertifikaten, die zum Verschlüsseln der Sicherheitsdomänen Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

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

### <span data-ttu-id="ca3f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3f3-115">-DefaultProfile</span></span>
<span data-ttu-id="ca3f3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca3f3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ca3f3-117">-Force</span></span>
<span data-ttu-id="ca3f3-118">Geben Sie an, ob vorhandene Datei überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="ca3f3-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca3f3-119">-InputObject</span></span>
<span data-ttu-id="ca3f3-120">Objekt, das ein verwaltetes HSM darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="ca3f3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ca3f3-121">-Name</span></span>
<span data-ttu-id="ca3f3-122">Name des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="ca3f3-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="ca3f3-123">-OutputPath</span></span>
<span data-ttu-id="ca3f3-124">Geben Sie den Pfad an, in den Sicherheitsdomänen Daten heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-124">Specify the path where security domain data will be downloaded to.</span></span>

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

### <span data-ttu-id="ca3f3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca3f3-125">-PassThru</span></span>
<span data-ttu-id="ca3f3-126">Wenn angegeben, wird ein boolescher Wert zurückgegeben, wenn das Cmdlet erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="ca3f3-127">-Quorum</span><span class="sxs-lookup"><span data-stu-id="ca3f3-127">-Quorum</span></span>
<span data-ttu-id="ca3f3-128">Die Mindestanzahl von Freigaben, die zum Entschlüsseln der Sicherheitsdomäne für die Wiederherstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

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

### <span data-ttu-id="ca3f3-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ca3f3-129">-Confirm</span></span>
<span data-ttu-id="ca3f3-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca3f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3f3-131">-WhatIf</span></span>
<span data-ttu-id="ca3f3-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca3f3-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca3f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3f3-134">CommonParameters</span></span>
<span data-ttu-id="ca3f3-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca3f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3f3-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca3f3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3f3-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca3f3-137">INPUTS</span></span>

### <span data-ttu-id="ca3f3-138">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ca3f3-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="ca3f3-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca3f3-139">OUTPUTS</span></span>

### <span data-ttu-id="ca3f3-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca3f3-140">System.Boolean</span></span>

## <span data-ttu-id="ca3f3-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca3f3-141">NOTES</span></span>

## <span data-ttu-id="ca3f3-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca3f3-142">RELATED LINKS</span></span>
