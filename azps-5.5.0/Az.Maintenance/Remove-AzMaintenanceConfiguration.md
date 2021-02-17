---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152369"
---
# <span data-ttu-id="f37c9-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f37c9-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="f37c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f37c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f37c9-103">Datensatz "Konfiguration löschen"</span><span class="sxs-lookup"><span data-stu-id="f37c9-103">Delete Configuration record</span></span>

## <span data-ttu-id="f37c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f37c9-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f37c9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f37c9-105">DESCRIPTION</span></span>
<span data-ttu-id="f37c9-106">Datensatz "Wartungskonfiguration löschen"</span><span class="sxs-lookup"><span data-stu-id="f37c9-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="f37c9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f37c9-107">EXAMPLES</span></span>

### <span data-ttu-id="f37c9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f37c9-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="f37c9-109">Datensatz "Wartungskonfiguration löschen"</span><span class="sxs-lookup"><span data-stu-id="f37c9-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="f37c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f37c9-110">PARAMETERS</span></span>

### <span data-ttu-id="f37c9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f37c9-111">-AsJob</span></span>
<span data-ttu-id="f37c9-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f37c9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f37c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37c9-113">-DefaultProfile</span></span>
<span data-ttu-id="f37c9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f37c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f37c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f37c9-115">-Force</span></span>
<span data-ttu-id="f37c9-116">Erzwingen Sie das Entfernen ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="f37c9-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="f37c9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f37c9-117">-Name</span></span>
<span data-ttu-id="f37c9-118">Der Name der Wartungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f37c9-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="f37c9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f37c9-119">-PassThru</span></span>
<span data-ttu-id="f37c9-120">Gibt den Status des Vorgangs "Entfernen" zurück.</span><span class="sxs-lookup"><span data-stu-id="f37c9-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="f37c9-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f37c9-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f37c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f37c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="f37c9-123">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f37c9-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="f37c9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f37c9-124">-Confirm</span></span>
<span data-ttu-id="f37c9-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f37c9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f37c9-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f37c9-126">-WhatIf</span></span>
<span data-ttu-id="f37c9-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f37c9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f37c9-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f37c9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f37c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37c9-129">CommonParameters</span></span>
<span data-ttu-id="f37c9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f37c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37c9-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f37c9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37c9-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f37c9-132">INPUTS</span></span>

### <span data-ttu-id="f37c9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f37c9-133">System.String</span></span>

## <span data-ttu-id="f37c9-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f37c9-134">OUTPUTS</span></span>

### <span data-ttu-id="f37c9-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f37c9-135">System.Boolean</span></span>

## <span data-ttu-id="f37c9-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f37c9-136">NOTES</span></span>

## <span data-ttu-id="f37c9-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f37c9-137">RELATED LINKS</span></span>
