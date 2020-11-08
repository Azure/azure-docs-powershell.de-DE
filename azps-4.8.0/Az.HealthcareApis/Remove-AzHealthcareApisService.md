---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 12db158089473c5f0cfb01e24b762ecf192f8991
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173581"
---
# <span data-ttu-id="2cc1c-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="2cc1c-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="2cc1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc1c-103">Löscht eine Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-103">Deletes a service instance.</span></span>

## <span data-ttu-id="2cc1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc1c-104">SYNTAX</span></span>

### <span data-ttu-id="2cc1c-105">ServiceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cc1c-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cc1c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cc1c-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cc1c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cc1c-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cc1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cc1c-108">DESCRIPTION</span></span>
<span data-ttu-id="2cc1c-109">Löscht eine Dienstinstanz.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-109">Deletes a service instance.</span></span>

## <span data-ttu-id="2cc1c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cc1c-110">EXAMPLES</span></span>

### <span data-ttu-id="2cc1c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2cc1c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="2cc1c-112">Löscht den vorhandenen HealthcareApis-Dienst mit dem angegebenen Namen innerhalb einer bereitgestellten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="2cc1c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2cc1c-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="2cc1c-114">Löscht den vorhandenen HealthcareApis-Dienst mit der bereitgestellten Quell-Nr.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="2cc1c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2cc1c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="2cc1c-116">Löscht das bereitgestellte HealthcareApis-Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="2cc1c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cc1c-117">PARAMETERS</span></span>

### <span data-ttu-id="2cc1c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cc1c-118">-AsJob</span></span>
<span data-ttu-id="2cc1c-119">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="2cc1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc1c-120">-DefaultProfile</span></span>
<span data-ttu-id="2cc1c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cc1c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2cc1c-122">-InputObject</span></span>
<span data-ttu-id="2cc1c-123">HealthcareApis-Dienstobjekt</span><span class="sxs-lookup"><span data-stu-id="2cc1c-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc1c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2cc1c-124">-Name</span></span>
<span data-ttu-id="2cc1c-125">Name des HealthcareApis-Diensts.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc1c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cc1c-126">-PassThru</span></span>
<span data-ttu-id="2cc1c-127">Wenn bereitgestellt, gibt true zurück, wenn der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="2cc1c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc1c-128">-ResourceGroupName</span></span>
<span data-ttu-id="2cc1c-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc1c-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2cc1c-130">-ResourceId</span></span>
<span data-ttu-id="2cc1c-131">HealthcareApis-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="2cc1c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2cc1c-132">-Confirm</span></span>
<span data-ttu-id="2cc1c-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cc1c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cc1c-134">-WhatIf</span></span>
<span data-ttu-id="2cc1c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cc1c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cc1c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc1c-137">CommonParameters</span></span>
<span data-ttu-id="2cc1c-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc1c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc1c-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cc1c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc1c-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cc1c-140">INPUTS</span></span>

### <span data-ttu-id="2cc1c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2cc1c-141">System.String</span></span>

### <span data-ttu-id="2cc1c-142">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="2cc1c-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="2cc1c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cc1c-143">OUTPUTS</span></span>

### <span data-ttu-id="2cc1c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cc1c-144">System.Boolean</span></span>

## <span data-ttu-id="2cc1c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cc1c-145">NOTES</span></span>

## <span data-ttu-id="2cc1c-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cc1c-146">RELATED LINKS</span></span>
