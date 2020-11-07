---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658088"
---
# <span data-ttu-id="16513-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="16513-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="16513-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="16513-102">SYNOPSIS</span></span>
<span data-ttu-id="16513-103">Löscht eine Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="16513-103">Deletes an attestation.</span></span>

## <span data-ttu-id="16513-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="16513-104">SYNTAX</span></span>

### <span data-ttu-id="16513-105">ByAvailableAttestation (Standard)</span><span class="sxs-lookup"><span data-stu-id="16513-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16513-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="16513-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16513-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="16513-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16513-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16513-108">DESCRIPTION</span></span>
<span data-ttu-id="16513-109">Das Remove-AzAttestation-Cmdlet löscht die angegebene Bescheinigung.</span><span class="sxs-lookup"><span data-stu-id="16513-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="16513-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="16513-110">EXAMPLES</span></span>

### <span data-ttu-id="16513-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16513-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="16513-112">Löschen Sie die Bescheinigung "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1".</span><span class="sxs-lookup"><span data-stu-id="16513-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="16513-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="16513-113">PARAMETERS</span></span>

### <span data-ttu-id="16513-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16513-114">-AsJob</span></span>
<span data-ttu-id="16513-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="16513-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16513-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16513-116">-DefaultProfile</span></span>
<span data-ttu-id="16513-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="16513-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16513-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="16513-118">-InputObject</span></span>
<span data-ttu-id="16513-119">Bescheinigungs Objekt, das gelöscht werden soll</span><span class="sxs-lookup"><span data-stu-id="16513-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16513-120">-Name</span><span class="sxs-lookup"><span data-stu-id="16513-120">-Name</span></span>
<span data-ttu-id="16513-121">Gibt den Namen der zu entfernenden Bescheinigung an.</span><span class="sxs-lookup"><span data-stu-id="16513-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16513-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16513-122">-PassThru</span></span>
<span data-ttu-id="16513-123">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="16513-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="16513-124">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="16513-124">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16513-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16513-125">-ResourceGroupName</span></span>
<span data-ttu-id="16513-126">Gibt den Namen der Ressourcengruppe für die zu entfernende Azure-Bescheinigung an.</span><span class="sxs-lookup"><span data-stu-id="16513-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16513-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="16513-127">-ResourceId</span></span>
<span data-ttu-id="16513-128">Bescheinigungs-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="16513-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16513-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="16513-129">-Confirm</span></span>
<span data-ttu-id="16513-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16513-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16513-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16513-131">-WhatIf</span></span>
<span data-ttu-id="16513-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16513-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16513-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16513-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16513-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16513-134">CommonParameters</span></span>
<span data-ttu-id="16513-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16513-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16513-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16513-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16513-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="16513-137">INPUTS</span></span>

### <span data-ttu-id="16513-138">System. String</span><span class="sxs-lookup"><span data-stu-id="16513-138">System.String</span></span>

### <span data-ttu-id="16513-139">Microsoft. Azure. Commands. Testat. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="16513-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="16513-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="16513-140">OUTPUTS</span></span>

### <span data-ttu-id="16513-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16513-141">System.Boolean</span></span>

## <span data-ttu-id="16513-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="16513-142">NOTES</span></span>

## <span data-ttu-id="16513-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="16513-143">RELATED LINKS</span></span>
