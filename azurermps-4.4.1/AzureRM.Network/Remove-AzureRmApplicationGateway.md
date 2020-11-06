---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: cd4824b73aa7fe7a80a3c4bccba37445a85c2c22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479058"
---
# <span data-ttu-id="adb6f-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adb6f-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="adb6f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="adb6f-102">SYNOPSIS</span></span>
<span data-ttu-id="adb6f-103">Entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="adb6f-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adb6f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="adb6f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adb6f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adb6f-105">DESCRIPTION</span></span>
<span data-ttu-id="adb6f-106">Das Cmdlet **Remove-AzureRmApplicationGateway** entfernt ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="adb6f-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="adb6f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="adb6f-107">EXAMPLES</span></span>

### <span data-ttu-id="adb6f-108">Beispiel 1: Entfernen eines angegebenen Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="adb6f-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="adb6f-109">Dieser Befehl entfernt das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="adb6f-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="adb6f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="adb6f-110">PARAMETERS</span></span>

### <span data-ttu-id="adb6f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="adb6f-111">-Force</span></span>
<span data-ttu-id="adb6f-112">Gibt an, dass das Cmdlet das Löschen des Anwendungs Gateways erzwingt, unabhängig davon, ob ihm Ressourcen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="adb6f-112">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adb6f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="adb6f-113">-Name</span></span>
<span data-ttu-id="adb6f-114">Gibt den Namen des Anwendungs Gateways an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adb6f-114">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="adb6f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adb6f-115">-PassThru</span></span>
<span data-ttu-id="adb6f-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="adb6f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="adb6f-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="adb6f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="adb6f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb6f-118">-ResourceGroupName</span></span>
<span data-ttu-id="adb6f-119">Gibt den Namen des Ressourcengruppen namens an, zu dem das Anwendungsgateway gehört.</span><span class="sxs-lookup"><span data-stu-id="adb6f-119">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="adb6f-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="adb6f-120">-Confirm</span></span>
<span data-ttu-id="adb6f-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="adb6f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb6f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb6f-122">-WhatIf</span></span>
<span data-ttu-id="adb6f-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="adb6f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb6f-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="adb6f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb6f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb6f-125">-DefaultProfile</span></span>
<span data-ttu-id="adb6f-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="adb6f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adb6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb6f-127">CommonParameters</span></span>
<span data-ttu-id="adb6f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb6f-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adb6f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb6f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="adb6f-130">INPUTS</span></span>

## <span data-ttu-id="adb6f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="adb6f-131">OUTPUTS</span></span>

### <span data-ttu-id="adb6f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="adb6f-132">System.String</span></span>

## <span data-ttu-id="adb6f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="adb6f-133">NOTES</span></span>

## <span data-ttu-id="adb6f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="adb6f-134">RELATED LINKS</span></span>

[<span data-ttu-id="adb6f-135">Satz-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adb6f-135">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


