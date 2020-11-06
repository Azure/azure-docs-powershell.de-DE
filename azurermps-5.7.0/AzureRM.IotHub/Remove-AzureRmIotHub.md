---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 1da7b9981b3c2fe96d895290b7ab73dfc36e183e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496517"
---
# <span data-ttu-id="1c03d-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="1c03d-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="1c03d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c03d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c03d-103">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="1c03d-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c03d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c03d-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c03d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c03d-105">DESCRIPTION</span></span>
<span data-ttu-id="1c03d-106">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="1c03d-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="1c03d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c03d-107">EXAMPLES</span></span>

### <span data-ttu-id="1c03d-108">Beispiel 1 Entfernen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="1c03d-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1c03d-109">Entfernt eine IotHub mit dem Namen "myiothub"</span><span class="sxs-lookup"><span data-stu-id="1c03d-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="1c03d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c03d-110">PARAMETERS</span></span>

### <span data-ttu-id="1c03d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c03d-111">-DefaultProfile</span></span>
<span data-ttu-id="1c03d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1c03d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c03d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1c03d-113">-Name</span></span>
<span data-ttu-id="1c03d-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="1c03d-114">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c03d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c03d-115">-ResourceGroupName</span></span>
<span data-ttu-id="1c03d-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="1c03d-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c03d-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c03d-117">-Confirm</span></span>
<span data-ttu-id="1c03d-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c03d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c03d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c03d-119">-WhatIf</span></span>
<span data-ttu-id="1c03d-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c03d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c03d-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c03d-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c03d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c03d-122">CommonParameters</span></span>
<span data-ttu-id="1c03d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c03d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c03d-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c03d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c03d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c03d-125">INPUTS</span></span>

### <span data-ttu-id="1c03d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1c03d-126">System.String</span></span>

## <span data-ttu-id="1c03d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c03d-127">OUTPUTS</span></span>

### <span data-ttu-id="1c03d-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="1c03d-128">System.Object</span></span>

## <span data-ttu-id="1c03d-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c03d-129">NOTES</span></span>

## <span data-ttu-id="1c03d-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c03d-130">RELATED LINKS</span></span>

