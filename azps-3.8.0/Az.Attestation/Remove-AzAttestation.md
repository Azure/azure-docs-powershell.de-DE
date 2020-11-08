---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997441"
---
# <span data-ttu-id="45542-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="45542-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="45542-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45542-102">SYNOPSIS</span></span>
<span data-ttu-id="45542-103">Löscht eine Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="45542-103">Deletes an attestation.</span></span>

## <span data-ttu-id="45542-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45542-104">SYNTAX</span></span>

### <span data-ttu-id="45542-105">ByAvailableAttestation (Standard)</span><span class="sxs-lookup"><span data-stu-id="45542-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45542-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="45542-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45542-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="45542-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45542-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45542-108">DESCRIPTION</span></span>
<span data-ttu-id="45542-109">Das Remove-AzAttestation-Cmdlet löscht die angegebene Bescheinigung.</span><span class="sxs-lookup"><span data-stu-id="45542-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="45542-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45542-110">EXAMPLES</span></span>

### <span data-ttu-id="45542-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="45542-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="45542-112">Löschen Sie den Zertifizierungsanbieter namens *pshtest3* in der Ressourcengruppe mit dem Namen *PSH-Test-RG* aus dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45542-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="45542-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="45542-113">PARAMETERS</span></span>

### <span data-ttu-id="45542-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45542-114">-DefaultProfile</span></span>
<span data-ttu-id="45542-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45542-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45542-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="45542-116">-InputObject</span></span>
<span data-ttu-id="45542-117">Bescheinigungs Objekt, das gelöscht werden soll</span><span class="sxs-lookup"><span data-stu-id="45542-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="45542-118">-Name</span><span class="sxs-lookup"><span data-stu-id="45542-118">-Name</span></span>
<span data-ttu-id="45542-119">Gibt den Namen der zu entfernenden Bescheinigung an.</span><span class="sxs-lookup"><span data-stu-id="45542-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="45542-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45542-120">-PassThru</span></span>
<span data-ttu-id="45542-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="45542-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="45542-122">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="45542-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="45542-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45542-123">-ResourceGroupName</span></span>
<span data-ttu-id="45542-124">Gibt den Namen der Ressourcengruppe für die zu entfernende Azure-Bescheinigung an.</span><span class="sxs-lookup"><span data-stu-id="45542-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="45542-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="45542-125">-ResourceId</span></span>
<span data-ttu-id="45542-126">Bescheinigungs-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="45542-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="45542-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="45542-127">-Confirm</span></span>
<span data-ttu-id="45542-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45542-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45542-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45542-129">-WhatIf</span></span>
<span data-ttu-id="45542-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45542-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45542-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45542-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45542-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45542-132">CommonParameters</span></span>
<span data-ttu-id="45542-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45542-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45542-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45542-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45542-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45542-135">INPUTS</span></span>

### <span data-ttu-id="45542-136">System. String</span><span class="sxs-lookup"><span data-stu-id="45542-136">System.String</span></span>

### <span data-ttu-id="45542-137">Microsoft. Azure. Commands. Testat. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="45542-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="45542-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45542-138">OUTPUTS</span></span>

### <span data-ttu-id="45542-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45542-139">System.Boolean</span></span>

## <span data-ttu-id="45542-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="45542-140">NOTES</span></span>

## <span data-ttu-id="45542-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45542-141">RELATED LINKS</span></span>
