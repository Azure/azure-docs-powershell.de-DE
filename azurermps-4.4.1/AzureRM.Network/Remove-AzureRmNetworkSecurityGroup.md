---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: fd6d9a09bd2c4fa597d2c384d3ba8e730b3f1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662769"
---
# <span data-ttu-id="4827c-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4827c-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="4827c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4827c-102">SYNOPSIS</span></span>
<span data-ttu-id="4827c-103">Entfernt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4827c-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4827c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4827c-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4827c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4827c-105">DESCRIPTION</span></span>
<span data-ttu-id="4827c-106">Das Cmdlet **Remove-AzureRmNetworkSecurityGroup** entfernt eine Azure Network Security-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4827c-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="4827c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4827c-107">EXAMPLES</span></span>

### <span data-ttu-id="4827c-108">Beispiel 1: Entfernen einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="4827c-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="4827c-109">Dieser Befehl entfernt die Sicherheitsgruppe mit dem Namen NSG-FrontEnd in der Ressourcengruppe mit dem Namen TestRG.</span><span class="sxs-lookup"><span data-stu-id="4827c-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="4827c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4827c-110">PARAMETERS</span></span>

### <span data-ttu-id="4827c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4827c-111">-Force</span></span>
<span data-ttu-id="4827c-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4827c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4827c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4827c-113">-Name</span></span>
<span data-ttu-id="4827c-114">Gibt den Namen der Netzwerksicherheitsgruppe an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4827c-114">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4827c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4827c-115">-PassThru</span></span>
<span data-ttu-id="4827c-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4827c-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4827c-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="4827c-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4827c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4827c-118">-ResourceGroupName</span></span>
<span data-ttu-id="4827c-119">Gibt den Namen einer Ressourcengruppe an, aus der dieses Cmdlet eine Netzwerksicherheitsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="4827c-119">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="4827c-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4827c-120">-Confirm</span></span>
<span data-ttu-id="4827c-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4827c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4827c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4827c-122">-WhatIf</span></span>
<span data-ttu-id="4827c-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4827c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4827c-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4827c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4827c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4827c-125">-DefaultProfile</span></span>
<span data-ttu-id="4827c-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4827c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4827c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4827c-127">CommonParameters</span></span>
<span data-ttu-id="4827c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4827c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4827c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4827c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4827c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4827c-130">INPUTS</span></span>

## <span data-ttu-id="4827c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4827c-131">OUTPUTS</span></span>

## <span data-ttu-id="4827c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="4827c-132">NOTES</span></span>

## <span data-ttu-id="4827c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4827c-133">RELATED LINKS</span></span>

[<span data-ttu-id="4827c-134">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4827c-134">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="4827c-135">Neu – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4827c-135">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="4827c-136">Satz-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4827c-136">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


