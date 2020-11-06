---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 3f7e0a96212e9de87c90cffd059801084da471ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495874"
---
# <span data-ttu-id="7765a-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7765a-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="7765a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7765a-102">SYNOPSIS</span></span>
<span data-ttu-id="7765a-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="7765a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7765a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7765a-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7765a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7765a-105">DESCRIPTION</span></span>
<span data-ttu-id="7765a-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="7765a-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7765a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7765a-107">EXAMPLES</span></span>

### <span data-ttu-id="7765a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7765a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7765a-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="7765a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7765a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7765a-110">PARAMETERS</span></span>

### <span data-ttu-id="7765a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7765a-111">-DefaultProfile</span></span>
<span data-ttu-id="7765a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7765a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7765a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7765a-113">-Force</span></span>
<span data-ttu-id="7765a-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="7765a-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7765a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7765a-115">-Name</span></span>
<span data-ttu-id="7765a-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7765a-116">The resource name.</span></span>

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

### <span data-ttu-id="7765a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7765a-117">-PassThru</span></span>
<span data-ttu-id="7765a-118">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="7765a-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7765a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7765a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7765a-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7765a-120">The resource group name.</span></span>

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

### <span data-ttu-id="7765a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7765a-121">-Confirm</span></span>
<span data-ttu-id="7765a-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7765a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7765a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7765a-123">-WhatIf</span></span>
<span data-ttu-id="7765a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7765a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7765a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7765a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7765a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7765a-126">CommonParameters</span></span>
<span data-ttu-id="7765a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7765a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7765a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7765a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7765a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7765a-129">INPUTS</span></span>

### <span data-ttu-id="7765a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7765a-130">System.String</span></span>

## <span data-ttu-id="7765a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7765a-131">OUTPUTS</span></span>

### <span data-ttu-id="7765a-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7765a-132">System.Boolean</span></span>

## <span data-ttu-id="7765a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7765a-133">NOTES</span></span>

## <span data-ttu-id="7765a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7765a-134">RELATED LINKS</span></span>
