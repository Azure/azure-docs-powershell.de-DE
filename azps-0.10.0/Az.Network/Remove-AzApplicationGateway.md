---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: 62d80f194fff8259d28f53d7957fef1a077f5389
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841236"
---
# <span data-ttu-id="995e1-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="995e1-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="995e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="995e1-102">SYNOPSIS</span></span>
<span data-ttu-id="995e1-103">Entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="995e1-103">Removes an application gateway.</span></span>

## <span data-ttu-id="995e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="995e1-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="995e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="995e1-105">DESCRIPTION</span></span>
<span data-ttu-id="995e1-106">Das Cmdlet **Remove-AzApplicationGateway** entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="995e1-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="995e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="995e1-107">EXAMPLES</span></span>

### <span data-ttu-id="995e1-108">Beispiel 1: Entfernen eines angegebenen Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="995e1-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="995e1-109">Dieser Befehl entfernt das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="995e1-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="995e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="995e1-110">PARAMETERS</span></span>

### <span data-ttu-id="995e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="995e1-111">-DefaultProfile</span></span>
<span data-ttu-id="995e1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="995e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="995e1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="995e1-113">-Force</span></span>
<span data-ttu-id="995e1-114">Gibt an, dass das Cmdlet das Löschen des Anwendungs Gateways erzwingt, unabhängig davon, ob ihm Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="995e1-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="995e1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="995e1-115">-Name</span></span>
<span data-ttu-id="995e1-116">Gibt den Namen des Anwendungs Gateways an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="995e1-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="995e1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="995e1-117">-PassThru</span></span>
<span data-ttu-id="995e1-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="995e1-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="995e1-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="995e1-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="995e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="995e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="995e1-121">Gibt den Namen des Ressourcengruppen namens an, zu dem das Anwendungsgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="995e1-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="995e1-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="995e1-122">-Confirm</span></span>
<span data-ttu-id="995e1-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="995e1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="995e1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="995e1-124">-WhatIf</span></span>
<span data-ttu-id="995e1-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="995e1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="995e1-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="995e1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="995e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="995e1-127">CommonParameters</span></span>
<span data-ttu-id="995e1-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="995e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="995e1-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="995e1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="995e1-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="995e1-130">INPUTS</span></span>

## <span data-ttu-id="995e1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="995e1-131">OUTPUTS</span></span>

### <span data-ttu-id="995e1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="995e1-132">System.String</span></span>

## <span data-ttu-id="995e1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="995e1-133">NOTES</span></span>

## <span data-ttu-id="995e1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="995e1-134">RELATED LINKS</span></span>

[<span data-ttu-id="995e1-135">Satz-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="995e1-135">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


