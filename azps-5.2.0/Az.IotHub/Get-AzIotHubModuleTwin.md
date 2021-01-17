---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307024"
---
# <span data-ttu-id="f88d7-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f88d7-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="f88d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f88d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f88d7-103">Ruft ein IoT-Gerätemodul-Modul ab.</span><span class="sxs-lookup"><span data-stu-id="f88d7-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="f88d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f88d7-104">SYNTAX</span></span>

### <span data-ttu-id="f88d7-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f88d7-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f88d7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f88d7-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f88d7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f88d7-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f88d7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f88d7-108">DESCRIPTION</span></span>
<span data-ttu-id="f88d7-109">Ruft ein IoT-Gerätemodul-Modul ab.</span><span class="sxs-lookup"><span data-stu-id="f88d7-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="f88d7-110">Weitere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins Informationen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="f88d7-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="f88d7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f88d7-111">EXAMPLES</span></span>

### <span data-ttu-id="f88d7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f88d7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="f88d7-113">Gibt das Gerätemodulmodulobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f88d7-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="f88d7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f88d7-114">PARAMETERS</span></span>

### <span data-ttu-id="f88d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88d7-115">-DefaultProfile</span></span>
<span data-ttu-id="f88d7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f88d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f88d7-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f88d7-117">-DeviceId</span></span>
<span data-ttu-id="f88d7-118">Zielgerät-ID.</span><span class="sxs-lookup"><span data-stu-id="f88d7-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f88d7-119">-InputObject</span></span>
<span data-ttu-id="f88d7-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="f88d7-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f88d7-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f88d7-121">-IotHubName</span></span>
<span data-ttu-id="f88d7-122">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="f88d7-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88d7-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="f88d7-123">-ModuleId</span></span>
<span data-ttu-id="f88d7-124">Zielmodul-ID.</span><span class="sxs-lookup"><span data-stu-id="f88d7-124">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f88d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="f88d7-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f88d7-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88d7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f88d7-127">-ResourceId</span></span>
<span data-ttu-id="f88d7-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f88d7-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f88d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88d7-129">CommonParameters</span></span>
<span data-ttu-id="f88d7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88d7-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f88d7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88d7-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f88d7-132">INPUTS</span></span>

### <span data-ttu-id="f88d7-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f88d7-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f88d7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f88d7-134">System.String</span></span>

## <span data-ttu-id="f88d7-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f88d7-135">OUTPUTS</span></span>

### <span data-ttu-id="f88d7-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="f88d7-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="f88d7-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f88d7-137">NOTES</span></span>

## <span data-ttu-id="f88d7-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f88d7-138">RELATED LINKS</span></span>
