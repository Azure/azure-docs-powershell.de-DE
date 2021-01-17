---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: fce61fd015271c9f6b5a3752fae33eaa80d6447c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361736"
---
# <span data-ttu-id="a40e8-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="a40e8-101">Update-AzIotHub</span></span>

## <span data-ttu-id="a40e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a40e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a40e8-103">Aktualisieren Sie einen Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="a40e8-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="a40e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a40e8-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a40e8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a40e8-105">DESCRIPTION</span></span>
<span data-ttu-id="a40e8-106">Sie können die Tageigenschaften eines IotHub aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a40e8-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="a40e8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a40e8-107">EXAMPLES</span></span>

### <span data-ttu-id="a40e8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a40e8-108">Example 1</span></span>
```
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -Tag $updatedTag

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiothub
Name           : myiothub
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[key0, value0]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="a40e8-109">Aktualisieren von Tags eines IoT-Hubs.</span><span class="sxs-lookup"><span data-stu-id="a40e8-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="a40e8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a40e8-110">PARAMETERS</span></span>

### <span data-ttu-id="a40e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40e8-111">-DefaultProfile</span></span>
<span data-ttu-id="a40e8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a40e8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a40e8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a40e8-113">-Name</span></span>
<span data-ttu-id="a40e8-114">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="a40e8-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a40e8-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="a40e8-115">-Reset</span></span>
<span data-ttu-id="a40e8-116">Zurücksetzen von IoTHub-Tags</span><span class="sxs-lookup"><span data-stu-id="a40e8-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="a40e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="a40e8-118">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a40e8-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a40e8-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="a40e8-119">-Tag</span></span>
<span data-ttu-id="a40e8-120">IoTHub-Tag-Sammlung</span><span class="sxs-lookup"><span data-stu-id="a40e8-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40e8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a40e8-121">-Confirm</span></span>
<span data-ttu-id="a40e8-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a40e8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a40e8-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a40e8-123">-WhatIf</span></span>
<span data-ttu-id="a40e8-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a40e8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a40e8-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a40e8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a40e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40e8-126">CommonParameters</span></span>
<span data-ttu-id="a40e8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40e8-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40e8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40e8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a40e8-129">INPUTS</span></span>

### <span data-ttu-id="a40e8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a40e8-130">System.String</span></span>

## <span data-ttu-id="a40e8-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a40e8-131">OUTPUTS</span></span>

### <span data-ttu-id="a40e8-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a40e8-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="a40e8-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a40e8-133">NOTES</span></span>

## <span data-ttu-id="a40e8-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a40e8-134">RELATED LINKS</span></span>
