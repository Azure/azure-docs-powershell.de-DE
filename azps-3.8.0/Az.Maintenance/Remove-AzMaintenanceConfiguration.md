---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004419"
---
# <span data-ttu-id="b3d95-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3d95-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="b3d95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3d95-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d95-103">Konfigurationseintrag löschen</span><span class="sxs-lookup"><span data-stu-id="b3d95-103">Delete Configuration record</span></span>

## <span data-ttu-id="b3d95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3d95-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3d95-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3d95-105">DESCRIPTION</span></span>
<span data-ttu-id="b3d95-106">Wartungs Konfigurationseintrag löschen</span><span class="sxs-lookup"><span data-stu-id="b3d95-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="b3d95-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3d95-107">EXAMPLES</span></span>

### <span data-ttu-id="b3d95-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3d95-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="b3d95-109">Wartungs Konfigurationseintrag löschen</span><span class="sxs-lookup"><span data-stu-id="b3d95-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="b3d95-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3d95-110">PARAMETERS</span></span>

### <span data-ttu-id="b3d95-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3d95-111">-AsJob</span></span>
<span data-ttu-id="b3d95-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b3d95-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3d95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d95-113">-DefaultProfile</span></span>
<span data-ttu-id="b3d95-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3d95-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d95-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b3d95-115">-Force</span></span>
<span data-ttu-id="b3d95-116">"Entfernen" ohne Bestätigung erzwingen.</span><span class="sxs-lookup"><span data-stu-id="b3d95-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="b3d95-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b3d95-117">-Name</span></span>
<span data-ttu-id="b3d95-118">Der Name der Wartungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b3d95-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="b3d95-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3d95-119">-PassThru</span></span>
<span data-ttu-id="b3d95-120">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="b3d95-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="b3d95-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b3d95-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3d95-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d95-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3d95-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3d95-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="b3d95-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3d95-124">-Confirm</span></span>
<span data-ttu-id="b3d95-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3d95-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3d95-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3d95-126">-WhatIf</span></span>
<span data-ttu-id="b3d95-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3d95-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3d95-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3d95-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3d95-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d95-129">CommonParameters</span></span>
<span data-ttu-id="b3d95-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d95-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d95-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3d95-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d95-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3d95-132">INPUTS</span></span>

### <span data-ttu-id="b3d95-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b3d95-133">System.String</span></span>

## <span data-ttu-id="b3d95-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3d95-134">OUTPUTS</span></span>

### <span data-ttu-id="b3d95-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3d95-135">System.Boolean</span></span>

## <span data-ttu-id="b3d95-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3d95-136">NOTES</span></span>

## <span data-ttu-id="b3d95-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3d95-137">RELATED LINKS</span></span>
