---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004420"
---
# <span data-ttu-id="ecd5c-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ecd5c-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="ecd5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd5c-103">Heben Sie die Registrierung der Konfiguration für die Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="ecd5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecd5c-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecd5c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecd5c-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd5c-106">Heben Sie die Registrierung der Konfiguration für die Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="ecd5c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecd5c-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd5c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ecd5c-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="ecd5c-109">Heben Sie die Registrierung der Konfiguration für die Ressource auf.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="ecd5c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecd5c-110">PARAMETERS</span></span>

### <span data-ttu-id="ecd5c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecd5c-111">-AsJob</span></span>
<span data-ttu-id="ecd5c-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ecd5c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ecd5c-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ecd5c-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="ecd5c-114">Der Name der Konfigurationsaufgabe.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="ecd5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd5c-115">-DefaultProfile</span></span>
<span data-ttu-id="ecd5c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecd5c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ecd5c-117">-Force</span></span>
<span data-ttu-id="ecd5c-118">"Entfernen" ohne Bestätigung erzwingen.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="ecd5c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecd5c-119">-PassThru</span></span>
<span data-ttu-id="ecd5c-120">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ecd5c-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ecd5c-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="ecd5c-122">-ProviderName</span></span>
<span data-ttu-id="ecd5c-123">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd5c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd5c-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecd5c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd5c-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ecd5c-126">-ResourceName</span></span>
<span data-ttu-id="ecd5c-127">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd5c-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="ecd5c-128">-ResourceParentName</span></span>
<span data-ttu-id="ecd5c-129">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd5c-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="ecd5c-130">-ResourceParentType</span></span>
<span data-ttu-id="ecd5c-131">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-131">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd5c-132">-</span><span class="sxs-lookup"><span data-stu-id="ecd5c-132">-ResourceType</span></span>
<span data-ttu-id="ecd5c-133">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd5c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecd5c-134">-Confirm</span></span>
<span data-ttu-id="ecd5c-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd5c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd5c-136">-WhatIf</span></span>
<span data-ttu-id="ecd5c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd5c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd5c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd5c-139">CommonParameters</span></span>
<span data-ttu-id="ecd5c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd5c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd5c-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecd5c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd5c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecd5c-142">INPUTS</span></span>

### <span data-ttu-id="ecd5c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd5c-143">System.String</span></span>

## <span data-ttu-id="ecd5c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecd5c-144">OUTPUTS</span></span>

### <span data-ttu-id="ecd5c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecd5c-145">System.Boolean</span></span>

## <span data-ttu-id="ecd5c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecd5c-146">NOTES</span></span>

## <span data-ttu-id="ecd5c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecd5c-147">RELATED LINKS</span></span>
