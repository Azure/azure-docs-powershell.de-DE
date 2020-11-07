---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 1529b7b70ec25a7ee8f4b047e28fe77efaf92351
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819736"
---
# <span data-ttu-id="2e191-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="2e191-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="2e191-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e191-102">SYNOPSIS</span></span>
<span data-ttu-id="2e191-103">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="2e191-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="2e191-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e191-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e191-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e191-105">DESCRIPTION</span></span>
<span data-ttu-id="2e191-106">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="2e191-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="2e191-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e191-107">EXAMPLES</span></span>

### <span data-ttu-id="2e191-108">Beispiel 1 Entfernen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="2e191-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2e191-109">Entfernt eine IotHub mit dem Namen "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2e191-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="2e191-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e191-110">PARAMETERS</span></span>

### <span data-ttu-id="2e191-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e191-111">-DefaultProfile</span></span>
<span data-ttu-id="2e191-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2e191-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e191-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2e191-113">-Name</span></span>
<span data-ttu-id="2e191-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="2e191-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="2e191-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e191-115">-ResourceGroupName</span></span>
<span data-ttu-id="2e191-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2e191-116">Resource Group Name</span></span>

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

### <span data-ttu-id="2e191-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e191-117">-Confirm</span></span>
<span data-ttu-id="2e191-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e191-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e191-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e191-119">-WhatIf</span></span>
<span data-ttu-id="2e191-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e191-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e191-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e191-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e191-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e191-122">CommonParameters</span></span>
<span data-ttu-id="2e191-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e191-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e191-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e191-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e191-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e191-125">INPUTS</span></span>

### <span data-ttu-id="2e191-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2e191-126">System.String</span></span>

## <span data-ttu-id="2e191-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e191-127">OUTPUTS</span></span>

### <span data-ttu-id="2e191-128">System. void</span><span class="sxs-lookup"><span data-stu-id="2e191-128">System.Void</span></span>

## <span data-ttu-id="2e191-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e191-129">NOTES</span></span>

## <span data-ttu-id="2e191-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e191-130">RELATED LINKS</span></span>
