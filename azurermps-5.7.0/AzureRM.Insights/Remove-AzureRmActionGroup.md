---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 1d4a5365ac2112364a544eb2481a3193f23519c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500590"
---
# <span data-ttu-id="65b30-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="65b30-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="65b30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65b30-102">SYNOPSIS</span></span>
<span data-ttu-id="65b30-103">Entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="65b30-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65b30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65b30-104">SYNTAX</span></span>

### <span data-ttu-id="65b30-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="65b30-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b30-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65b30-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65b30-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65b30-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b30-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65b30-108">DESCRIPTION</span></span>
<span data-ttu-id="65b30-109">Das Cmdlet **Remove-AzureRmActionGroup** entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="65b30-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="65b30-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65b30-110">EXAMPLES</span></span>

### <span data-ttu-id="65b30-111">Beispiel 1: Entfernen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="65b30-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="65b30-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="65b30-112">PARAMETERS</span></span>

### <span data-ttu-id="65b30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b30-113">-DefaultProfile</span></span>
<span data-ttu-id="65b30-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="65b30-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65b30-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65b30-115">-InputObject</span></span>
<span data-ttu-id="65b30-116">Aktionsgruppe resourc</span><span class="sxs-lookup"><span data-stu-id="65b30-116">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65b30-117">-Name</span><span class="sxs-lookup"><span data-stu-id="65b30-117">-Name</span></span>
<span data-ttu-id="65b30-118">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="65b30-118">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b30-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b30-119">-ResourceGroupName</span></span>
<span data-ttu-id="65b30-120">Die Ressourcengruppe Nam</span><span class="sxs-lookup"><span data-stu-id="65b30-120">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b30-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="65b30-121">-ResourceId</span></span>
<span data-ttu-id="65b30-122">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="65b30-122">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65b30-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65b30-123">-Confirm</span></span>
<span data-ttu-id="65b30-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65b30-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b30-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b30-125">-WhatIf</span></span>
<span data-ttu-id="65b30-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65b30-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65b30-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65b30-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65b30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b30-128">CommonParameters</span></span>
<span data-ttu-id="65b30-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b30-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b30-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65b30-131">INPUTS</span></span>

### <span data-ttu-id="65b30-132">Keine</span><span class="sxs-lookup"><span data-stu-id="65b30-132">None</span></span>
<span data-ttu-id="65b30-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="65b30-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65b30-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65b30-134">OUTPUTS</span></span>

### <span data-ttu-id="65b30-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="65b30-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="65b30-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="65b30-136">NOTES</span></span>

## <span data-ttu-id="65b30-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65b30-137">RELATED LINKS</span></span>

<span data-ttu-id="65b30-138">[Satz-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Neu – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="65b30-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
