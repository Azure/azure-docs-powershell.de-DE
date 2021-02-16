---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149449"
---
# <span data-ttu-id="cf7ed-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="cf7ed-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="cf7ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7ed-103">Löscht einen Nachweis.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-103">Deletes an attestation.</span></span>

## <span data-ttu-id="cf7ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf7ed-104">SYNTAX</span></span>

### <span data-ttu-id="cf7ed-105">ByAvailableAttestation (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf7ed-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf7ed-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="cf7ed-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf7ed-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="cf7ed-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf7ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf7ed-108">DESCRIPTION</span></span>
<span data-ttu-id="cf7ed-109">Das Remove-AzAttestation cmdlet löscht den angegebenen Nachweis.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="cf7ed-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf7ed-110">EXAMPLES</span></span>

### <span data-ttu-id="cf7ed-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf7ed-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="cf7ed-112">Löschen Sie den Nachweisanbieter namens *"pshtest3"* in der Ressourcengruppe *"psh-test-rg"* aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="cf7ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf7ed-113">PARAMETERS</span></span>

### <span data-ttu-id="cf7ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf7ed-114">-DefaultProfile</span></span>
<span data-ttu-id="cf7ed-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf7ed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf7ed-116">-InputObject</span></span>
<span data-ttu-id="cf7ed-117">Das zu löschende Nachweisobjekt.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="cf7ed-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cf7ed-118">-Name</span></span>
<span data-ttu-id="cf7ed-119">Gibt den Namen des zu entfernenden Nachweises an.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="cf7ed-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf7ed-120">-PassThru</span></span>
<span data-ttu-id="cf7ed-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cf7ed-122">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cf7ed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf7ed-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf7ed-124">Gibt den Namen der Ressourcengruppe an, die für den zu entfernenden Azure-Nachweis entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="cf7ed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf7ed-125">-ResourceId</span></span>
<span data-ttu-id="cf7ed-126">Nachweisressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="cf7ed-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf7ed-127">-Confirm</span></span>
<span data-ttu-id="cf7ed-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf7ed-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cf7ed-129">-WhatIf</span></span>
<span data-ttu-id="cf7ed-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf7ed-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf7ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7ed-132">CommonParameters</span></span>
<span data-ttu-id="cf7ed-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf7ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7ed-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf7ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7ed-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf7ed-135">INPUTS</span></span>

### <span data-ttu-id="cf7ed-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cf7ed-136">System.String</span></span>

### <span data-ttu-id="cf7ed-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="cf7ed-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="cf7ed-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf7ed-138">OUTPUTS</span></span>

### <span data-ttu-id="cf7ed-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cf7ed-139">System.Boolean</span></span>

## <span data-ttu-id="cf7ed-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf7ed-140">NOTES</span></span>

## <span data-ttu-id="cf7ed-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf7ed-141">RELATED LINKS</span></span>
