---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180030"
---
# <span data-ttu-id="dbf57-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="dbf57-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="dbf57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbf57-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf57-103">Entfernt eine Vorlagenspezifikation</span><span class="sxs-lookup"><span data-stu-id="dbf57-103">Removes a Template Spec</span></span>

## <span data-ttu-id="dbf57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbf57-104">SYNTAX</span></span>

### <span data-ttu-id="dbf57-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbf57-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf57-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf57-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf57-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbf57-107">DESCRIPTION</span></span>
<span data-ttu-id="dbf57-108">Entfernt eine angegebene Vorlagenspezifikation. Wenn der Parameter Version **-Version** angegeben ist, wird nur die angegebene Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="dbf57-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="dbf57-109">Wenn keine bestimmte Version bereitgestellt wird, werden die Vorlagenspezifikation und alle Ihre Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="dbf57-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="dbf57-110">Wenn das Flag **-Force** vorhanden ist, wird keine Bestätigungsaufforderung zum Entfernen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dbf57-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="dbf57-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbf57-111">EXAMPLES</span></span>

### <span data-ttu-id="dbf57-112">Beispiel 1: Entfernen einer bestimmten Version nach Name</span><span class="sxs-lookup"><span data-stu-id="dbf57-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="dbf57-113">Entfernt die Version "v 1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="dbf57-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="dbf57-114">Beispiel 2: Entfernen einer bestimmten Version nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dbf57-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="dbf57-115">Entfernt die Version "v 1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" des Abonnement- \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="dbf57-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="dbf57-116">Beispiel 3: Entfernen einer Vorlagenspezifikation und aller Versionen nach Namen</span><span class="sxs-lookup"><span data-stu-id="dbf57-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="dbf57-117">Entfernt die Vorlagenspezifikation mit dem Namen "MyTemplateSpec" und alle Versionen in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="dbf57-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="dbf57-118">Beispiel 3: Entfernen einer Vorlagenspezifikation und aller Versionen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dbf57-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="dbf57-119">Entfernt die Vorlagenspezifikation mit dem Namen "MyTemplateSpec" und alle Ihre Versionen innerhalb der Ressourcengruppe "myRG" des Abonnement- \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="dbf57-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="dbf57-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbf57-120">PARAMETERS</span></span>

### <span data-ttu-id="dbf57-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf57-121">-DefaultProfile</span></span>
<span data-ttu-id="dbf57-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbf57-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf57-123">-Force</span><span class="sxs-lookup"><span data-stu-id="dbf57-123">-Force</span></span>
<span data-ttu-id="dbf57-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="dbf57-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dbf57-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dbf57-125">-Name</span></span>
<span data-ttu-id="dbf57-126">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="dbf57-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf57-127">-ResourceGroupName</span></span>
<span data-ttu-id="dbf57-128">Der Name der Ressourcengruppe der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="dbf57-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf57-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dbf57-129">-ResourceId</span></span>
<span data-ttu-id="dbf57-130">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="dbf57-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf57-131">-Version</span><span class="sxs-lookup"><span data-stu-id="dbf57-131">-Version</span></span>
<span data-ttu-id="dbf57-132">Die Version der Vorlagenspezifikation, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbf57-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf57-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbf57-133">-Confirm</span></span>
<span data-ttu-id="dbf57-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbf57-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf57-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf57-135">-WhatIf</span></span>
<span data-ttu-id="dbf57-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbf57-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbf57-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbf57-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf57-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf57-138">CommonParameters</span></span>
<span data-ttu-id="dbf57-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf57-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf57-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbf57-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf57-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbf57-141">INPUTS</span></span>

### <span data-ttu-id="dbf57-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dbf57-142">System.String</span></span>

## <span data-ttu-id="dbf57-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbf57-143">OUTPUTS</span></span>

### <span data-ttu-id="dbf57-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbf57-144">System.Boolean</span></span>

## <span data-ttu-id="dbf57-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbf57-145">NOTES</span></span>

## <span data-ttu-id="dbf57-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbf57-146">RELATED LINKS</span></span>
