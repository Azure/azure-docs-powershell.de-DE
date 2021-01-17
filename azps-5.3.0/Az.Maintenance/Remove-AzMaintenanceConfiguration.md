---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467664"
---
# <span data-ttu-id="812a0-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="812a0-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="812a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="812a0-102">SYNOPSIS</span></span>
<span data-ttu-id="812a0-103">Datensatz "Konfiguration löschen"</span><span class="sxs-lookup"><span data-stu-id="812a0-103">Delete Configuration record</span></span>

## <span data-ttu-id="812a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="812a0-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="812a0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="812a0-105">DESCRIPTION</span></span>
<span data-ttu-id="812a0-106">Datensatz "Wartungskonfiguration löschen"</span><span class="sxs-lookup"><span data-stu-id="812a0-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="812a0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="812a0-107">EXAMPLES</span></span>

### <span data-ttu-id="812a0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="812a0-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="812a0-109">Datensatz "Wartungskonfiguration löschen"</span><span class="sxs-lookup"><span data-stu-id="812a0-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="812a0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="812a0-110">PARAMETERS</span></span>

### <span data-ttu-id="812a0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="812a0-111">-AsJob</span></span>
<span data-ttu-id="812a0-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="812a0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="812a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812a0-113">-DefaultProfile</span></span>
<span data-ttu-id="812a0-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="812a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="812a0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="812a0-115">-Force</span></span>
<span data-ttu-id="812a0-116">Erzwingen Sie das Entfernen ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="812a0-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="812a0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="812a0-117">-Name</span></span>
<span data-ttu-id="812a0-118">Der Name der Wartungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="812a0-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="812a0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="812a0-119">-PassThru</span></span>
<span data-ttu-id="812a0-120">Gibt den Status des Vorgangs "Entfernen" zurück.</span><span class="sxs-lookup"><span data-stu-id="812a0-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="812a0-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="812a0-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="812a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="812a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="812a0-123">Der Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="812a0-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="812a0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="812a0-124">-Confirm</span></span>
<span data-ttu-id="812a0-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="812a0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="812a0-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="812a0-126">-WhatIf</span></span>
<span data-ttu-id="812a0-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="812a0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="812a0-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="812a0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="812a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812a0-129">CommonParameters</span></span>
<span data-ttu-id="812a0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="812a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812a0-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="812a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812a0-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="812a0-132">INPUTS</span></span>

### <span data-ttu-id="812a0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="812a0-133">System.String</span></span>

## <span data-ttu-id="812a0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="812a0-134">OUTPUTS</span></span>

### <span data-ttu-id="812a0-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="812a0-135">System.Boolean</span></span>

## <span data-ttu-id="812a0-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="812a0-136">NOTES</span></span>

## <span data-ttu-id="812a0-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="812a0-137">RELATED LINKS</span></span>
