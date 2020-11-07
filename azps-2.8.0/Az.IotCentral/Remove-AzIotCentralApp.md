---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 6043daf907331b970744daffe716e4bbdbc1d6f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651006"
---
# <span data-ttu-id="9dc2d-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="9dc2d-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="9dc2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9dc2d-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc2d-103">Löscht eine viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="9dc2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dc2d-104">SYNTAX</span></span>

### <span data-ttu-id="9dc2d-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9dc2d-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dc2d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dc2d-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dc2d-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dc2d-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dc2d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9dc2d-108">DESCRIPTION</span></span>
<span data-ttu-id="9dc2d-109">Löscht eine vorhandene viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="9dc2d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9dc2d-110">EXAMPLES</span></span>

### <span data-ttu-id="9dc2d-111">Beispiel 1 DELETE und viele zentrale Anwendung</span><span class="sxs-lookup"><span data-stu-id="9dc2d-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="9dc2d-112">Löscht die bereitgestellte Central-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="9dc2d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dc2d-113">PARAMETERS</span></span>

### <span data-ttu-id="9dc2d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dc2d-114">-AsJob</span></span>
<span data-ttu-id="9dc2d-115">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="9dc2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc2d-116">-DefaultProfile</span></span>
<span data-ttu-id="9dc2d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dc2d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9dc2d-118">-InputObject</span></span>
<span data-ttu-id="9dc2d-119">Viel zentrales Anwendungs Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc2d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9dc2d-120">-Name</span></span>
<span data-ttu-id="9dc2d-121">Der Name der zentralen Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc2d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dc2d-122">-PassThru</span></span>
<span data-ttu-id="9dc2d-123">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="9dc2d-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9dc2d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dc2d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9dc2d-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc2d-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9dc2d-126">-ResourceId</span></span>
<span data-ttu-id="9dc2d-127">Ressourcen-ID der zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc2d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9dc2d-128">-Confirm</span></span>
<span data-ttu-id="9dc2d-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc2d-130">-WhatIf</span></span>
<span data-ttu-id="9dc2d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc2d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc2d-133">CommonParameters</span></span>
<span data-ttu-id="9dc2d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dc2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc2d-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dc2d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc2d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9dc2d-136">INPUTS</span></span>

### <span data-ttu-id="9dc2d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9dc2d-137">System.String</span></span>

### <span data-ttu-id="9dc2d-138">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="9dc2d-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="9dc2d-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9dc2d-139">OUTPUTS</span></span>

### <span data-ttu-id="9dc2d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9dc2d-140">System.Boolean</span></span>

## <span data-ttu-id="9dc2d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9dc2d-141">NOTES</span></span>

## <span data-ttu-id="9dc2d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9dc2d-142">RELATED LINKS</span></span>
