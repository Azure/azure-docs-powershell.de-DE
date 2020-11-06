---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/remove-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Remove-AzureRmIotCentralApp.md
ms.openlocfilehash: c8a2f32b82a6111c1117a4134f0f7fe8b96a966f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505378"
---
# <span data-ttu-id="bf41a-101">Remove-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="bf41a-101">Remove-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="bf41a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf41a-102">SYNOPSIS</span></span>
<span data-ttu-id="bf41a-103">Löscht eine viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bf41a-103">Deletes an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf41a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf41a-104">SYNTAX</span></span>

### <span data-ttu-id="bf41a-105">ResourceIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf41a-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf41a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf41a-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf41a-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf41a-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzureRmIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf41a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf41a-108">DESCRIPTION</span></span>
<span data-ttu-id="bf41a-109">Löscht eine vorhandene viel zentrale Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bf41a-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="bf41a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf41a-110">EXAMPLES</span></span>

### <span data-ttu-id="bf41a-111">Beispiel 1 DELETE und viele zentrale Anwendung</span><span class="sxs-lookup"><span data-stu-id="bf41a-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="bf41a-112">Löscht die bereitgestellte Central-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bf41a-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="bf41a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf41a-113">PARAMETERS</span></span>

### <span data-ttu-id="bf41a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf41a-114">-AsJob</span></span>
<span data-ttu-id="bf41a-115">Führen Sie das Cmdlet als Job im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="bf41a-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="bf41a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf41a-116">-DefaultProfile</span></span>
<span data-ttu-id="bf41a-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf41a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf41a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf41a-118">-InputObject</span></span>
<span data-ttu-id="bf41a-119">Viel zentrales Anwendungs Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="bf41a-119">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf41a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bf41a-120">-Name</span></span>
<span data-ttu-id="bf41a-121">Der Name der zentralen Anwendungsressource.</span><span class="sxs-lookup"><span data-stu-id="bf41a-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf41a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf41a-122">-PassThru</span></span>
<span data-ttu-id="bf41a-123">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="bf41a-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bf41a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf41a-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf41a-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bf41a-125">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf41a-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bf41a-126">-ResourceId</span></span>
<span data-ttu-id="bf41a-127">Ressourcen-ID der zentralen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bf41a-127">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf41a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf41a-128">-Confirm</span></span>
<span data-ttu-id="bf41a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf41a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf41a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf41a-130">-WhatIf</span></span>
<span data-ttu-id="bf41a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf41a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf41a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf41a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf41a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf41a-133">CommonParameters</span></span>
<span data-ttu-id="bf41a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf41a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf41a-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf41a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf41a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf41a-136">INPUTS</span></span>

### <span data-ttu-id="bf41a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bf41a-137">System.String</span></span>
### <span data-ttu-id="bf41a-138">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="bf41a-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="bf41a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf41a-139">OUTPUTS</span></span>

### <span data-ttu-id="bf41a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf41a-140">System.Boolean</span></span>
## <span data-ttu-id="bf41a-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf41a-141">NOTES</span></span>

## <span data-ttu-id="bf41a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf41a-142">RELATED LINKS</span></span>
