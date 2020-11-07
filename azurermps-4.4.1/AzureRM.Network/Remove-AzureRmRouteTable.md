---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: 17cd4ab4e60156c1ab4d6dd4357e638ddaf2c5a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662768"
---
# <span data-ttu-id="c7cc0-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7cc0-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="c7cc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="c7cc0-103">Entfernt eine Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7cc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7cc0-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7cc0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="c7cc0-106">Das Cmdlet **Remove-AzureRmRouteTable** entfernt eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="c7cc0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="c7cc0-108">Beispiel 1: Entfernen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="c7cc0-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="c7cc0-109">Dieser Befehl entfernt die Routingtabelle mit dem Namen RouteTable01 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="c7cc0-110">Das Cmdlet fordert Sie zur Bestätigung auf, bevor die Tabelle entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="c7cc0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7cc0-111">PARAMETERS</span></span>

### <span data-ttu-id="c7cc0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c7cc0-112">-Force</span></span>
<span data-ttu-id="c7cc0-113">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c7cc0-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c7cc0-114">-Name</span></span>
<span data-ttu-id="c7cc0-115">Gibt den Namen der Arbeitsplan Tabelle an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-115">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7cc0-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7cc0-116">-PassThru</span></span>
<span data-ttu-id="c7cc0-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c7cc0-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c7cc0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7cc0-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7cc0-120">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet entfernte Arbeitsplan Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-120">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c7cc0-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7cc0-121">-Confirm</span></span>
<span data-ttu-id="c7cc0-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7cc0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7cc0-123">-WhatIf</span></span>
<span data-ttu-id="c7cc0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7cc0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7cc0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7cc0-126">-DefaultProfile</span></span>
<span data-ttu-id="c7cc0-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7cc0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7cc0-128">CommonParameters</span></span>
<span data-ttu-id="c7cc0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7cc0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7cc0-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7cc0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7cc0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7cc0-131">INPUTS</span></span>

## <span data-ttu-id="c7cc0-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7cc0-132">OUTPUTS</span></span>

## <span data-ttu-id="c7cc0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7cc0-133">NOTES</span></span>

## <span data-ttu-id="c7cc0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7cc0-134">RELATED LINKS</span></span>

[<span data-ttu-id="c7cc0-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7cc0-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="c7cc0-136">Neu – AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7cc0-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="c7cc0-137">Satz-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7cc0-137">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


