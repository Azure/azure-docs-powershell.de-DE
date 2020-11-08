---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: a2b8d83254c84ee974173611912dd9b21cb7a26d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997428"
---
# <span data-ttu-id="ea59a-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="ea59a-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="ea59a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea59a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea59a-103">Setzt die Richtlinie von einem Mandanten in Azure Attestationn.} zurück</span><span class="sxs-lookup"><span data-stu-id="ea59a-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="ea59a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea59a-104">SYNTAX</span></span>

### <span data-ttu-id="ea59a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea59a-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea59a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea59a-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea59a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea59a-107">DESCRIPTION</span></span>
<span data-ttu-id="ea59a-108">Das Reset-AzAttestationPolicy-Cmdlet setzt die benutzerdefinierte Bescheinigungs Richtlinie von einem Mandanten in Azure-Bescheinigung zurück.</span><span class="sxs-lookup"><span data-stu-id="ea59a-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="ea59a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea59a-109">EXAMPLES</span></span>

### <span data-ttu-id="ea59a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea59a-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="ea59a-111">Setzen Sie die Richtlinie auf die Standardeinstellung für den Bescheinigungs Anbieter *pshtest* für Tee-Typ *SgxEnclave* zurück.</span><span class="sxs-lookup"><span data-stu-id="ea59a-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="ea59a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea59a-112">PARAMETERS</span></span>

### <span data-ttu-id="ea59a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea59a-113">-DefaultProfile</span></span>
<span data-ttu-id="ea59a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea59a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea59a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ea59a-115">-Name</span></span>
<span data-ttu-id="ea59a-116">Gibt den Namen des Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="ea59a-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="ea59a-117">Mit diesem Cmdlet wird die Richtlinie für den Mandanten zurückgesetzt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ea59a-117">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea59a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea59a-118">-PassThru</span></span>
<span data-ttu-id="ea59a-119">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ea59a-119">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ea59a-120">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="ea59a-120">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ea59a-121">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="ea59a-121">-Policy</span></span>
<span data-ttu-id="ea59a-122">Gibt das JSON-webtoken an, in dem das zurückzusetzende Richtliniendokument beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ea59a-122">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="ea59a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea59a-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea59a-124">Gibt den Namen der Ressourcengruppe eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="ea59a-124">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="ea59a-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ea59a-125">-ResourceId</span></span>
<span data-ttu-id="ea59a-126">Gibt die Resourcen-Nr eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="ea59a-126">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="ea59a-127">-Tee</span><span class="sxs-lookup"><span data-stu-id="ea59a-127">-Tee</span></span>
<span data-ttu-id="ea59a-128">Gibt einen Typ einer vertrauenswürdigen Ausführungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="ea59a-128">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="ea59a-129">Wir unterstützen vier Arten von Umgebungen: SgxEnclave, openenklave, CyResComponent und VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="ea59a-129">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="ea59a-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea59a-130">-Confirm</span></span>
<span data-ttu-id="ea59a-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea59a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea59a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea59a-132">-WhatIf</span></span>
<span data-ttu-id="ea59a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea59a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea59a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea59a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea59a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea59a-135">CommonParameters</span></span>
<span data-ttu-id="ea59a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea59a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea59a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea59a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea59a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea59a-138">INPUTS</span></span>

### <span data-ttu-id="ea59a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea59a-139">System.String</span></span>

## <span data-ttu-id="ea59a-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea59a-140">OUTPUTS</span></span>

### <span data-ttu-id="ea59a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea59a-141">System.Boolean</span></span>

## <span data-ttu-id="ea59a-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea59a-142">NOTES</span></span>

## <span data-ttu-id="ea59a-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea59a-143">RELATED LINKS</span></span>
