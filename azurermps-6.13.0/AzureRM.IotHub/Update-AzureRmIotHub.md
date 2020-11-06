---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/update-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
ms.openlocfilehash: 6a71c2318a709eb8d4b3fe2fe68a760919097aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503641"
---
# <span data-ttu-id="9079a-101">Update-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="9079a-101">Update-AzureRmIotHub</span></span>

## <span data-ttu-id="9079a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9079a-102">SYNOPSIS</span></span>
<span data-ttu-id="9079a-103">Aktualisieren eines Azure viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="9079a-103">Update an Azure IoT Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9079a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9079a-104">SYNTAX</span></span>

```
Update-AzureRmIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9079a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9079a-105">DESCRIPTION</span></span>
<span data-ttu-id="9079a-106">Sie können die Tags-Eigenschaften eines IotHub aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9079a-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="9079a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9079a-107">EXAMPLES</span></span>

### <span data-ttu-id="9079a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9079a-108">Example 1</span></span>
```
PS C:\> Update-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="9079a-109">Fügen Sie " @tags " zum Tag eines Azure-viel-Hubs "myiotdps" hinzu.</span><span class="sxs-lookup"><span data-stu-id="9079a-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="9079a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9079a-110">PARAMETERS</span></span>

### <span data-ttu-id="9079a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9079a-111">-DefaultProfile</span></span>
<span data-ttu-id="9079a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9079a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9079a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9079a-113">-Name</span></span>
<span data-ttu-id="9079a-114">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="9079a-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9079a-115">-Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="9079a-115">-Reset</span></span>
<span data-ttu-id="9079a-116">Zurücksetzen von IoTHub-Tags</span><span class="sxs-lookup"><span data-stu-id="9079a-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="9079a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9079a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9079a-118">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9079a-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9079a-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="9079a-119">-Tag</span></span>
<span data-ttu-id="9079a-120">IoTHub-Tag-Sammlung</span><span class="sxs-lookup"><span data-stu-id="9079a-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="9079a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9079a-121">-Confirm</span></span>
<span data-ttu-id="9079a-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9079a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9079a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9079a-123">-WhatIf</span></span>
<span data-ttu-id="9079a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9079a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9079a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9079a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9079a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9079a-126">CommonParameters</span></span>
<span data-ttu-id="9079a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9079a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9079a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9079a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9079a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9079a-129">INPUTS</span></span>

### <span data-ttu-id="9079a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9079a-130">System.String</span></span>

## <span data-ttu-id="9079a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9079a-131">OUTPUTS</span></span>

### <span data-ttu-id="9079a-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9079a-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="9079a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9079a-133">NOTES</span></span>

## <span data-ttu-id="9079a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9079a-134">RELATED LINKS</span></span>
