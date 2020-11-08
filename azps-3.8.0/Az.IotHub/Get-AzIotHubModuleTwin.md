---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004041"
---
# <span data-ttu-id="4ace9-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="4ace9-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="4ace9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ace9-102">SYNOPSIS</span></span>
<span data-ttu-id="4ace9-103">Ruft ein viel Gerätemodul Twin ab.</span><span class="sxs-lookup"><span data-stu-id="4ace9-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="4ace9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ace9-104">SYNTAX</span></span>

### <span data-ttu-id="4ace9-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ace9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ace9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ace9-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ace9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ace9-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ace9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ace9-108">DESCRIPTION</span></span>
<span data-ttu-id="4ace9-109">Ruft ein viel Gerätemodul Twin ab.</span><span class="sxs-lookup"><span data-stu-id="4ace9-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="4ace9-110">Weitere Informationen finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins .</span><span class="sxs-lookup"><span data-stu-id="4ace9-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="4ace9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ace9-111">EXAMPLES</span></span>

### <span data-ttu-id="4ace9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ace9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="4ace9-113">Gibt das Doppel Objekt des Geräte Moduls zurück.</span><span class="sxs-lookup"><span data-stu-id="4ace9-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="4ace9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ace9-114">PARAMETERS</span></span>

### <span data-ttu-id="4ace9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ace9-115">-DefaultProfile</span></span>
<span data-ttu-id="4ace9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ace9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ace9-117">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="4ace9-117">-DeviceId</span></span>
<span data-ttu-id="4ace9-118">Zielgeräte-ID.</span><span class="sxs-lookup"><span data-stu-id="4ace9-118">Target Device Id.</span></span>

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

### <span data-ttu-id="4ace9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ace9-119">-InputObject</span></span>
<span data-ttu-id="4ace9-120">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="4ace9-120">IotHub object</span></span>

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

### <span data-ttu-id="4ace9-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4ace9-121">-IotHubName</span></span>
<span data-ttu-id="4ace9-122">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="4ace9-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4ace9-123">-Modul-Nr</span><span class="sxs-lookup"><span data-stu-id="4ace9-123">-ModuleId</span></span>
<span data-ttu-id="4ace9-124">Ziel Modul-ID.</span><span class="sxs-lookup"><span data-stu-id="4ace9-124">Target Module Id.</span></span>

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

### <span data-ttu-id="4ace9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ace9-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ace9-126">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4ace9-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ace9-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4ace9-127">-ResourceId</span></span>
<span data-ttu-id="4ace9-128">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4ace9-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4ace9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ace9-129">CommonParameters</span></span>
<span data-ttu-id="4ace9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ace9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ace9-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ace9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ace9-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ace9-132">INPUTS</span></span>

### <span data-ttu-id="4ace9-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4ace9-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4ace9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4ace9-134">System.String</span></span>

## <span data-ttu-id="4ace9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ace9-135">OUTPUTS</span></span>

### <span data-ttu-id="4ace9-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="4ace9-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="4ace9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ace9-137">NOTES</span></span>

## <span data-ttu-id="4ace9-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ace9-138">RELATED LINKS</span></span>
