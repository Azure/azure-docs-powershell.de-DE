---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 3ba9706c452c293dea6ad6a0e23a51ccb03ada9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166593"
---
# <span data-ttu-id="a4bd2-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="a4bd2-101">Update-AzIotHub</span></span>

## <span data-ttu-id="a4bd2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bd2-103">Aktualisieren eines Azure viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="a4bd2-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="a4bd2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4bd2-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4bd2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="a4bd2-106">Sie können die Tags-Eigenschaften eines IotHub aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a4bd2-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="a4bd2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="a4bd2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4bd2-108">Example 1</span></span>
```
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="a4bd2-109">Fügen Sie " @tags " zum Tag eines Azure-viel-Hubs "myiotdps" hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4bd2-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="a4bd2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="a4bd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bd2-111">-DefaultProfile</span></span>
<span data-ttu-id="a4bd2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4bd2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4bd2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a4bd2-113">-Name</span></span>
<span data-ttu-id="a4bd2-114">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="a4bd2-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a4bd2-115">-Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="a4bd2-115">-Reset</span></span>
<span data-ttu-id="a4bd2-116">Zurücksetzen von IoTHub-Tags</span><span class="sxs-lookup"><span data-stu-id="a4bd2-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="a4bd2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4bd2-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4bd2-118">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a4bd2-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a4bd2-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4bd2-119">-Tag</span></span>
<span data-ttu-id="a4bd2-120">IoTHub-Tag-Sammlung</span><span class="sxs-lookup"><span data-stu-id="a4bd2-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="a4bd2-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a4bd2-121">-Confirm</span></span>
<span data-ttu-id="a4bd2-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4bd2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4bd2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4bd2-123">-WhatIf</span></span>
<span data-ttu-id="a4bd2-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4bd2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4bd2-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4bd2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4bd2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bd2-126">CommonParameters</span></span>
<span data-ttu-id="a4bd2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4bd2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bd2-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4bd2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bd2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4bd2-129">INPUTS</span></span>

### <span data-ttu-id="a4bd2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a4bd2-130">System.String</span></span>

## <span data-ttu-id="a4bd2-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4bd2-131">OUTPUTS</span></span>

### <span data-ttu-id="a4bd2-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a4bd2-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="a4bd2-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4bd2-133">NOTES</span></span>

## <span data-ttu-id="a4bd2-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4bd2-134">RELATED LINKS</span></span>
