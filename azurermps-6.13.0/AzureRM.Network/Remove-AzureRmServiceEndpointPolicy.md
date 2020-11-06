---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503509"
---
# <span data-ttu-id="72761-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="72761-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="72761-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72761-102">SYNOPSIS</span></span>
<span data-ttu-id="72761-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="72761-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72761-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72761-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72761-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72761-105">DESCRIPTION</span></span>
<span data-ttu-id="72761-106">Das Cmdlet **Remove-AzureRmServiceEndpointPolicy** entfernt eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="72761-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="72761-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72761-107">EXAMPLES</span></span>

### <span data-ttu-id="72761-108">Beispiel 1: entfernt eine Dienstendpunkt-Richtlinie mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="72761-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="72761-109">Mit diesem Befehl wird eine Dienstendpunkt-Richtlinie mit dem Namen Fischereipolitik1, der zu ResourceGroup gehört, mit dem Namen "resourcegroup1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="72761-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="72761-110">Beispiel 2: Entfernen einer Dienstendpunkt Richtlinie mithilfe des Eingabeobjekts</span><span class="sxs-lookup"><span data-stu-id="72761-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="72761-111">Dieser Befehl entfernt ein Dienstendpunkt-Richtlinienobjekt Fischereipolitik1, das zu ResourceGroup gehört, mit dem Namen "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="72761-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="72761-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="72761-112">PARAMETERS</span></span>

### <span data-ttu-id="72761-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72761-113">-DefaultProfile</span></span>
<span data-ttu-id="72761-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72761-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72761-115">-Force</span><span class="sxs-lookup"><span data-stu-id="72761-115">-Force</span></span>
<span data-ttu-id="72761-116">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="72761-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72761-117">-Name</span><span class="sxs-lookup"><span data-stu-id="72761-117">-Name</span></span>
<span data-ttu-id="72761-118">Der Name der Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="72761-118">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72761-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72761-119">-PassThru</span></span>
<span data-ttu-id="72761-120">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="72761-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72761-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72761-121">-ResourceGroupName</span></span>
<span data-ttu-id="72761-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72761-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72761-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72761-123">-Confirm</span></span>
<span data-ttu-id="72761-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72761-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72761-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72761-125">-WhatIf</span></span>
<span data-ttu-id="72761-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72761-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72761-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72761-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72761-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72761-128">CommonParameters</span></span>
<span data-ttu-id="72761-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72761-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="72761-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72761-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72761-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72761-131">INPUTS</span></span>

### <span data-ttu-id="72761-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72761-132">System.String</span></span>


## <span data-ttu-id="72761-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72761-133">OUTPUTS</span></span>

### <span data-ttu-id="72761-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="72761-134">System.Object</span></span>

## <span data-ttu-id="72761-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="72761-135">NOTES</span></span>

## <span data-ttu-id="72761-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72761-136">RELATED LINKS</span></span>
