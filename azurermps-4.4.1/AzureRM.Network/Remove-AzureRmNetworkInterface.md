---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 3250aa7f9108436cadbf0f46ab0e36d3a9c094d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477141"
---
# <span data-ttu-id="cd967-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd967-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="cd967-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd967-102">SYNOPSIS</span></span>
<span data-ttu-id="cd967-103">Entfernt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cd967-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd967-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd967-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd967-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd967-105">DESCRIPTION</span></span>
<span data-ttu-id="cd967-106">Das Cmdlet **Remove-AzureRmNetworkInterface** entfernt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cd967-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="cd967-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd967-107">EXAMPLES</span></span>

### <span data-ttu-id="cd967-108">Beispiel 1: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="cd967-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="cd967-109">Dieser Befehl entfernt die Netzwerkschnittstellen-NetworkInterface1 in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="cd967-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="cd967-110">Da der Parameter *Force* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="cd967-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="cd967-111">Beispiel 2: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="cd967-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="cd967-112">Dieser Befehl entfernt alle Netzwerkschnittstellen in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="cd967-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="cd967-113">Da der Parameter *Force* verwendet wird, wird der Benutzer nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="cd967-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="cd967-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd967-114">PARAMETERS</span></span>

### <span data-ttu-id="cd967-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd967-115">-Force</span></span>
<span data-ttu-id="cd967-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="cd967-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd967-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cd967-117">-Name</span></span>
<span data-ttu-id="cd967-118">Gibt den Namen der Netzwerkschnittstelle an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="cd967-118">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cd967-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd967-119">-PassThru</span></span>
<span data-ttu-id="cd967-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cd967-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd967-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="cd967-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd967-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd967-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd967-123">Gibt den Namen einer Ressourcengruppe an, die die vom Cmdlet entfernte Netzwerkschnittstelle enthält.</span><span class="sxs-lookup"><span data-stu-id="cd967-123">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cd967-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd967-124">-Confirm</span></span>
<span data-ttu-id="cd967-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd967-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd967-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd967-126">-WhatIf</span></span>
<span data-ttu-id="cd967-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd967-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd967-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd967-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd967-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd967-129">-DefaultProfile</span></span>
<span data-ttu-id="cd967-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd967-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd967-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd967-131">CommonParameters</span></span>
<span data-ttu-id="cd967-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd967-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd967-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd967-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd967-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd967-134">INPUTS</span></span>

## <span data-ttu-id="cd967-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd967-135">OUTPUTS</span></span>

## <span data-ttu-id="cd967-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd967-136">NOTES</span></span>

## <span data-ttu-id="cd967-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd967-137">RELATED LINKS</span></span>

[<span data-ttu-id="cd967-138">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd967-138">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="cd967-139">Neu – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd967-139">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="cd967-140">Satz-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cd967-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


