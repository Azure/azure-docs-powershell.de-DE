---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004008"
---
# <span data-ttu-id="8a230-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="8a230-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="8a230-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a230-102">SYNOPSIS</span></span>
<span data-ttu-id="8a230-103">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="8a230-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="8a230-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a230-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a230-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a230-105">DESCRIPTION</span></span>
<span data-ttu-id="8a230-106">Löscht eine IotHub.</span><span class="sxs-lookup"><span data-stu-id="8a230-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="8a230-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a230-107">EXAMPLES</span></span>

### <span data-ttu-id="8a230-108">Beispiel 1 Entfernen eines IotHub</span><span class="sxs-lookup"><span data-stu-id="8a230-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="8a230-109">Entfernt eine IotHub mit dem Namen "myiothub"</span><span class="sxs-lookup"><span data-stu-id="8a230-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="8a230-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a230-110">PARAMETERS</span></span>

### <span data-ttu-id="8a230-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a230-111">-DefaultProfile</span></span>
<span data-ttu-id="8a230-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8a230-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a230-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8a230-113">-Name</span></span>
<span data-ttu-id="8a230-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="8a230-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="8a230-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a230-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a230-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8a230-116">Resource Group Name</span></span>

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

### <span data-ttu-id="8a230-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a230-117">-Confirm</span></span>
<span data-ttu-id="8a230-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a230-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a230-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a230-119">-WhatIf</span></span>
<span data-ttu-id="8a230-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a230-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a230-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a230-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a230-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a230-122">CommonParameters</span></span>
<span data-ttu-id="8a230-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a230-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a230-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a230-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a230-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a230-125">INPUTS</span></span>

### <span data-ttu-id="8a230-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8a230-126">System.String</span></span>

## <span data-ttu-id="8a230-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a230-127">OUTPUTS</span></span>

### <span data-ttu-id="8a230-128">System. void</span><span class="sxs-lookup"><span data-stu-id="8a230-128">System.Void</span></span>

## <span data-ttu-id="8a230-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a230-129">NOTES</span></span>

## <span data-ttu-id="8a230-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a230-130">RELATED LINKS</span></span>
