---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 674105b31c06d3def687bfc58f8b16be1c6b86f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496070"
---
# <span data-ttu-id="212e7-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="212e7-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="212e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="212e7-102">SYNOPSIS</span></span>
<span data-ttu-id="212e7-103">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="212e7-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="212e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="212e7-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="212e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="212e7-105">DESCRIPTION</span></span>
<span data-ttu-id="212e7-106">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="212e7-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="212e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="212e7-107">EXAMPLES</span></span>

### <span data-ttu-id="212e7-108">Beispiel 1 Entfernen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="212e7-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="212e7-109">Entfernt eine IotHub mit dem Namen "myiothub"</span><span class="sxs-lookup"><span data-stu-id="212e7-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="212e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="212e7-110">PARAMETERS</span></span>

### <span data-ttu-id="212e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212e7-111">-DefaultProfile</span></span>
<span data-ttu-id="212e7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="212e7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="212e7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="212e7-113">-Name</span></span>
<span data-ttu-id="212e7-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="212e7-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="212e7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="212e7-115">-ResourceGroupName</span></span>
<span data-ttu-id="212e7-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="212e7-116">Resource Group Name</span></span>

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

### <span data-ttu-id="212e7-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="212e7-117">-Confirm</span></span>
<span data-ttu-id="212e7-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="212e7-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212e7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212e7-119">-WhatIf</span></span>
<span data-ttu-id="212e7-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="212e7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="212e7-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="212e7-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212e7-122">CommonParameters</span></span>
<span data-ttu-id="212e7-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212e7-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="212e7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212e7-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="212e7-125">INPUTS</span></span>

### <span data-ttu-id="212e7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="212e7-126">System.String</span></span>

## <span data-ttu-id="212e7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="212e7-127">OUTPUTS</span></span>

### <span data-ttu-id="212e7-128">System. void</span><span class="sxs-lookup"><span data-stu-id="212e7-128">System.Void</span></span>

## <span data-ttu-id="212e7-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="212e7-129">NOTES</span></span>

## <span data-ttu-id="212e7-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="212e7-130">RELATED LINKS</span></span>
