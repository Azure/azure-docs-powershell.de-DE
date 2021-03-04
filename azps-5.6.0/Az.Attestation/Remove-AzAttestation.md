---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 564c3d9a67e3a006a7ce7871419e236a71838a42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925224"
---
# <span data-ttu-id="ed52c-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="ed52c-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="ed52c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed52c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed52c-103">Löscht eine Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="ed52c-103">Deletes an attestation.</span></span>

## <span data-ttu-id="ed52c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed52c-104">SYNTAX</span></span>

### <span data-ttu-id="ed52c-105">ByAvailableAttestation (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed52c-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed52c-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="ed52c-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed52c-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="ed52c-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed52c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed52c-108">DESCRIPTION</span></span>
<span data-ttu-id="ed52c-109">Das Remove-AzAttestation cmdlet löscht die angegebene Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="ed52c-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="ed52c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed52c-110">EXAMPLES</span></span>

### <span data-ttu-id="ed52c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed52c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="ed52c-112">Löschen Sie den Nachweisanbieter mit dem Namen *pshtest3* in der Ressourcengruppe mit dem Namen *psh-test-rg* aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed52c-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="ed52c-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ed52c-113">PARAMETERS</span></span>

### <span data-ttu-id="ed52c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed52c-114">-DefaultProfile</span></span>
<span data-ttu-id="ed52c-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed52c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed52c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed52c-116">-InputObject</span></span>
<span data-ttu-id="ed52c-117">Das zu löschende Attestierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ed52c-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed52c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ed52c-118">-Name</span></span>
<span data-ttu-id="ed52c-119">Gibt den Namen der zu entfernenden Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="ed52c-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed52c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed52c-120">-PassThru</span></span>
<span data-ttu-id="ed52c-121">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ed52c-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ed52c-122">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="ed52c-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ed52c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed52c-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed52c-124">Gibt den Namen der Ressourcengruppe für azure attestation an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed52c-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed52c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed52c-125">-ResourceId</span></span>
<span data-ttu-id="ed52c-126">Nachweisressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ed52c-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed52c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed52c-127">-Confirm</span></span>
<span data-ttu-id="ed52c-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed52c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed52c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed52c-129">-WhatIf</span></span>
<span data-ttu-id="ed52c-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed52c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed52c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed52c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed52c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed52c-132">CommonParameters</span></span>
<span data-ttu-id="ed52c-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed52c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed52c-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed52c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed52c-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed52c-135">INPUTS</span></span>

### <span data-ttu-id="ed52c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ed52c-136">System.String</span></span>

### <span data-ttu-id="ed52c-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="ed52c-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="ed52c-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed52c-138">OUTPUTS</span></span>

### <span data-ttu-id="ed52c-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed52c-139">System.Boolean</span></span>

## <span data-ttu-id="ed52c-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ed52c-140">NOTES</span></span>

## <span data-ttu-id="ed52c-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ed52c-141">RELATED LINKS</span></span>
