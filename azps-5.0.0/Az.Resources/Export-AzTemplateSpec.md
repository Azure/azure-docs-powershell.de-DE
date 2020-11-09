---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300580"
---
# <span data-ttu-id="0fced-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="0fced-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="0fced-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fced-102">SYNOPSIS</span></span>
<span data-ttu-id="0fced-103">Exportiert eine Vorlagenspezifikation in das lokale Dateisystem</span><span class="sxs-lookup"><span data-stu-id="0fced-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="0fced-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fced-104">SYNTAX</span></span>

### <span data-ttu-id="0fced-105">ExportByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0fced-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fced-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fced-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fced-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fced-107">DESCRIPTION</span></span>
<span data-ttu-id="0fced-108">Exportiert eine bestimmte Vorlagen Spezifikationsversion in das lokale Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="0fced-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="0fced-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fced-109">EXAMPLES</span></span>

### <span data-ttu-id="0fced-110">Beispiel 1: Exportieren nach Name</span><span class="sxs-lookup"><span data-stu-id="0fced-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="0fced-111">Exportiert Version "v 1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" in den lokalen Ausgabeordner "V1".</span><span class="sxs-lookup"><span data-stu-id="0fced-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="0fced-112">Beispiel 2: Exportieren nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0fced-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="0fced-113">Exportiert Version "v 1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" des Abonnement- \{ subId \} in den lokalen Ausgabeordner "V1".</span><span class="sxs-lookup"><span data-stu-id="0fced-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="0fced-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fced-114">PARAMETERS</span></span>

### <span data-ttu-id="0fced-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fced-115">-DefaultProfile</span></span>
<span data-ttu-id="0fced-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fced-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fced-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0fced-117">-Name</span></span>
<span data-ttu-id="0fced-118">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="0fced-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fced-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="0fced-119">-OutputFolder</span></span>
<span data-ttu-id="0fced-120">Der Pfad zu dem Ordner, in dem die Vorlage spec-Version ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0fced-120">The path to the folder where the template spec version will be output to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fced-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fced-121">-ResourceGroupName</span></span>
<span data-ttu-id="0fced-122">Der Name der Ressourcengruppe der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="0fced-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fced-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0fced-123">-ResourceId</span></span>
<span data-ttu-id="0fced-124">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="0fced-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fced-125">-Version</span><span class="sxs-lookup"><span data-stu-id="0fced-125">-Version</span></span>
<span data-ttu-id="0fced-126">Die Version der Vorlagenspezifikation, die exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fced-126">The version of the template spec to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fced-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0fced-127">-Confirm</span></span>
<span data-ttu-id="0fced-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fced-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fced-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fced-129">-WhatIf</span></span>
<span data-ttu-id="0fced-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fced-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fced-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fced-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fced-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fced-132">CommonParameters</span></span>
<span data-ttu-id="0fced-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fced-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fced-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fced-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fced-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fced-135">INPUTS</span></span>

### <span data-ttu-id="0fced-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0fced-136">System.String</span></span>

## <span data-ttu-id="0fced-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fced-137">OUTPUTS</span></span>

### <span data-ttu-id="0fced-138">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0fced-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0fced-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fced-139">NOTES</span></span>

## <span data-ttu-id="0fced-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fced-140">RELATED LINKS</span></span>
