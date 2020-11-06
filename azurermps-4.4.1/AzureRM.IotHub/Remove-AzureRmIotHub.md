---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501825"
---
# <span data-ttu-id="59cd8-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="59cd8-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="59cd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="59cd8-103">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="59cd8-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59cd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59cd8-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59cd8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="59cd8-106">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="59cd8-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="59cd8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="59cd8-108">Beispiel 1 Entfernen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="59cd8-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="59cd8-109">Entfernt eine IotHub mit dem Namen "myiothub"</span><span class="sxs-lookup"><span data-stu-id="59cd8-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="59cd8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59cd8-110">PARAMETERS</span></span>

### <span data-ttu-id="59cd8-111">-Name</span><span class="sxs-lookup"><span data-stu-id="59cd8-111">-Name</span></span>
<span data-ttu-id="59cd8-112">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="59cd8-112">Name of the IotHub</span></span>

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

### <span data-ttu-id="59cd8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59cd8-113">-ResourceGroupName</span></span>
<span data-ttu-id="59cd8-114">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="59cd8-114">Resource Group Name</span></span>

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

### <span data-ttu-id="59cd8-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59cd8-115">-Confirm</span></span>
<span data-ttu-id="59cd8-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59cd8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59cd8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59cd8-117">-WhatIf</span></span>
<span data-ttu-id="59cd8-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59cd8-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59cd8-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59cd8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59cd8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59cd8-120">-DefaultProfile</span></span>
<span data-ttu-id="59cd8-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59cd8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59cd8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59cd8-122">CommonParameters</span></span>
<span data-ttu-id="59cd8-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59cd8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59cd8-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59cd8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59cd8-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59cd8-125">INPUTS</span></span>

### <span data-ttu-id="59cd8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="59cd8-126">System.String</span></span>

## <span data-ttu-id="59cd8-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59cd8-127">OUTPUTS</span></span>

### <span data-ttu-id="59cd8-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="59cd8-128">System.Object</span></span>

## <span data-ttu-id="59cd8-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="59cd8-129">NOTES</span></span>

## <span data-ttu-id="59cd8-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59cd8-130">RELATED LINKS</span></span>

