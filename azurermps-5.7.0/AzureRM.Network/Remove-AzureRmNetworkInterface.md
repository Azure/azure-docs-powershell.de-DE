---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 829dc03dad037b6b1576613ab18d9929a777241e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478409"
---
# <span data-ttu-id="1ed20-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1ed20-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="1ed20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ed20-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed20-103">Entfernt eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1ed20-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ed20-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed20-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ed20-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed20-106">Das Cmdlet **Remove-AzureRmNetworkInterface** entfernt eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1ed20-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="1ed20-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ed20-107">EXAMPLES</span></span>

### <span data-ttu-id="1ed20-108">Beispiel 1: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="1ed20-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="1ed20-109">Dieser Befehl entfernt die Netzwerkschnittstellen-NetworkInterface1 in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="1ed20-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="1ed20-110">Da der Parameter *Force* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="1ed20-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="1ed20-111">Beispiel 2: Entfernen einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="1ed20-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="1ed20-112">Dieser Befehl entfernt alle Netzwerkschnittstellen in der Ressourcengruppe ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="1ed20-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="1ed20-113">Da der Parameter *Force* verwendet wird, wird der Benutzer nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="1ed20-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="1ed20-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ed20-114">PARAMETERS</span></span>

### <span data-ttu-id="1ed20-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ed20-115">-AsJob</span></span>
<span data-ttu-id="1ed20-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1ed20-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ed20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed20-117">-DefaultProfile</span></span>
<span data-ttu-id="1ed20-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ed20-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ed20-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1ed20-119">-Force</span></span>
<span data-ttu-id="1ed20-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1ed20-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ed20-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1ed20-121">-Name</span></span>
<span data-ttu-id="1ed20-122">Gibt den Namen der Netzwerkschnittstelle an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1ed20-122">Specifies the name of the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ed20-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ed20-123">-PassThru</span></span>
<span data-ttu-id="1ed20-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ed20-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1ed20-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="1ed20-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1ed20-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed20-126">-ResourceGroupName</span></span>
<span data-ttu-id="1ed20-127">Gibt den Namen einer Ressourcengruppe an, die die vom Cmdlet entfernte Netzwerkschnittstelle enthält.</span><span class="sxs-lookup"><span data-stu-id="1ed20-127">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ed20-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ed20-128">-Confirm</span></span>
<span data-ttu-id="1ed20-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ed20-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed20-130">-WhatIf</span></span>
<span data-ttu-id="1ed20-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ed20-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed20-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ed20-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed20-133">CommonParameters</span></span>
<span data-ttu-id="1ed20-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed20-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed20-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed20-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ed20-136">INPUTS</span></span>

### <span data-ttu-id="1ed20-137">Keine</span><span class="sxs-lookup"><span data-stu-id="1ed20-137">None</span></span>
<span data-ttu-id="1ed20-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1ed20-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ed20-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ed20-139">OUTPUTS</span></span>

## <span data-ttu-id="1ed20-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ed20-140">NOTES</span></span>

## <span data-ttu-id="1ed20-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ed20-141">RELATED LINKS</span></span>

[<span data-ttu-id="1ed20-142">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1ed20-142">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="1ed20-143">Neu – AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1ed20-143">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="1ed20-144">Satz-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1ed20-144">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


