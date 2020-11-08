---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: f743b408917e575005589598a49fafbd8cc95379
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180401"
---
# <span data-ttu-id="f7f43-101">Restore-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="f7f43-101">Restore-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="f7f43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7f43-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f43-103">Wiederherstellen vorheriger gesicherter Sicherheitsdomänen Daten für ein verwaltetes HSM</span><span class="sxs-lookup"><span data-stu-id="f7f43-103">Restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="f7f43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7f43-104">SYNTAX</span></span>

### <span data-ttu-id="f7f43-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7f43-105">ByName (Default)</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f43-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f7f43-106">ByInputObject</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7f43-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7f43-107">DESCRIPTION</span></span>
<span data-ttu-id="f7f43-108">Mit diesem Cmdlet werden frühere gesicherte Sicherheitsdomänen Daten für ein verwaltetes HSM wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f7f43-108">This cmdlet restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="f7f43-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7f43-109">EXAMPLES</span></span>

### <span data-ttu-id="f7f43-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7f43-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Restore-AzManagedHsmSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="f7f43-111">Zunächst müssen die Schlüssel bereitgestellt werden, um die Sicherheitsdomänen Daten zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="f7f43-111">First, the keys need be provided to decrypt the security domain data.</span></span> <span data-ttu-id="f7f43-112">Anschließend werden mit dem Befehl **Restore-AzManagedHsmSecurityDomain** frühere gesicherte Sicherheitsdomänen Daten für ein verwaltetes HSM mithilfe dieser Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f7f43-112">Then, The **Restore-AzManagedHsmSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="f7f43-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7f43-113">PARAMETERS</span></span>

### <span data-ttu-id="f7f43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f43-114">-DefaultProfile</span></span>
<span data-ttu-id="f7f43-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7f43-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f43-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f7f43-116">-InputObject</span></span>
<span data-ttu-id="f7f43-117">Objekt, das ein verwaltetes HSM darstellt.</span><span class="sxs-lookup"><span data-stu-id="f7f43-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="f7f43-118">-Keys</span><span class="sxs-lookup"><span data-stu-id="f7f43-118">-Keys</span></span>
<span data-ttu-id="f7f43-119">Informationen zu den Schlüsseln, die zum Entschlüsseln der Sicherheitsdomänen Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7f43-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="f7f43-120">Sehen Sie sich die Beispiele für Ihre Konstruktion an.</span><span class="sxs-lookup"><span data-stu-id="f7f43-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="f7f43-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f7f43-121">-Name</span></span>
<span data-ttu-id="f7f43-122">Name des verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="f7f43-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="f7f43-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7f43-123">-PassThru</span></span>
<span data-ttu-id="f7f43-124">Wenn angegeben, wird ein boolescher Wert zurückgegeben, wenn das Cmdlet erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f7f43-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="f7f43-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="f7f43-125">-SecurityDomainPath</span></span>
<span data-ttu-id="f7f43-126">Geben Sie den Pfad zu den verschlüsselten Sicherheitsdomänen Daten an.</span><span class="sxs-lookup"><span data-stu-id="f7f43-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="f7f43-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7f43-127">-Confirm</span></span>
<span data-ttu-id="f7f43-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7f43-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f43-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f43-129">-WhatIf</span></span>
<span data-ttu-id="f7f43-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f43-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f43-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7f43-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f43-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f43-132">CommonParameters</span></span>
<span data-ttu-id="f7f43-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f43-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f43-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7f43-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f43-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7f43-135">INPUTS</span></span>

### <span data-ttu-id="f7f43-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f7f43-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="f7f43-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7f43-137">OUTPUTS</span></span>

### <span data-ttu-id="f7f43-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7f43-138">System.Boolean</span></span>

## <span data-ttu-id="f7f43-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7f43-139">NOTES</span></span>

## <span data-ttu-id="f7f43-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7f43-140">RELATED LINKS</span></span>
