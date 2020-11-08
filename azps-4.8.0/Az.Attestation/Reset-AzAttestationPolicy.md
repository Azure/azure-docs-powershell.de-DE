---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165345"
---
# <span data-ttu-id="cdd41-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="cdd41-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="cdd41-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdd41-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd41-103">Setzt die Richtlinie von einem Mandanten in Azure Attestationn.} zurück</span><span class="sxs-lookup"><span data-stu-id="cdd41-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="cdd41-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdd41-104">SYNTAX</span></span>

### <span data-ttu-id="cdd41-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdd41-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdd41-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdd41-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd41-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdd41-107">DESCRIPTION</span></span>
<span data-ttu-id="cdd41-108">Das Reset-AzAttestationPolicy-Cmdlet setzt die benutzerdefinierte Bescheinigungs Richtlinie von einem Mandanten in Azure-Bescheinigung zurück.</span><span class="sxs-lookup"><span data-stu-id="cdd41-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="cdd41-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdd41-109">EXAMPLES</span></span>

### <span data-ttu-id="cdd41-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cdd41-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="cdd41-111">Setzen Sie die Richtlinie auf die Standardeinstellung für den Bescheinigungs Anbieter *pshtest* für Tee-Typ *SgxEnclave* zurück.</span><span class="sxs-lookup"><span data-stu-id="cdd41-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="cdd41-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cdd41-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="cdd41-113">Wenn der Bescheinigungs Anbieter *pshtest* für die Verwendung des isolierten Vertrauensmodells konfiguriert ist, setzen Sie die Richtlinie auf den Standardwert für Tee-Typ *SgxEnclave* , indem Sie eine signierte Richtlinie einschließen.</span><span class="sxs-lookup"><span data-stu-id="cdd41-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="cdd41-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdd41-114">PARAMETERS</span></span>

### <span data-ttu-id="cdd41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd41-115">-DefaultProfile</span></span>
<span data-ttu-id="cdd41-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdd41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd41-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cdd41-117">-Name</span></span>
<span data-ttu-id="cdd41-118">Gibt den Namen des Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="cdd41-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="cdd41-119">Mit diesem Cmdlet wird die Richtlinie für den Mandanten zurückgesetzt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cdd41-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd41-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdd41-120">-PassThru</span></span>
<span data-ttu-id="cdd41-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="cdd41-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cdd41-122">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cdd41-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cdd41-123">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="cdd41-123">-Policy</span></span>
<span data-ttu-id="cdd41-124">Gibt das JSON-webtoken an, in dem das zurückzusetzende Richtliniendokument beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="cdd41-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd41-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd41-125">-ResourceGroupName</span></span>
<span data-ttu-id="cdd41-126">Gibt den Namen der Ressourcengruppe eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="cdd41-126">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd41-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cdd41-127">-ResourceId</span></span>
<span data-ttu-id="cdd41-128">Gibt die Resourcen-Nr eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="cdd41-128">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd41-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="cdd41-129">-Tee</span></span>
<span data-ttu-id="cdd41-130">Gibt einen Typ einer vertrauenswürdigen Ausführungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="cdd41-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="cdd41-131">Wir unterstützen vier Arten von Umgebungen: SgxEnclave, openenklave, CyResComponent und VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="cdd41-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="cdd41-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cdd41-132">-Confirm</span></span>
<span data-ttu-id="cdd41-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdd41-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd41-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd41-134">-WhatIf</span></span>
<span data-ttu-id="cdd41-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdd41-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd41-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdd41-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd41-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd41-137">CommonParameters</span></span>
<span data-ttu-id="cdd41-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd41-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd41-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdd41-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd41-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdd41-140">INPUTS</span></span>

### <span data-ttu-id="cdd41-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cdd41-141">System.String</span></span>

## <span data-ttu-id="cdd41-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdd41-142">OUTPUTS</span></span>

### <span data-ttu-id="cdd41-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdd41-143">System.Boolean</span></span>

## <span data-ttu-id="cdd41-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdd41-144">NOTES</span></span>

## <span data-ttu-id="cdd41-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdd41-145">RELATED LINKS</span></span>
