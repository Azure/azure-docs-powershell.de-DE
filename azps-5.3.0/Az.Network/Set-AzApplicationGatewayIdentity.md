---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378677"
---
# <span data-ttu-id="6f050-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="6f050-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="6f050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f050-102">SYNOPSIS</span></span>
<span data-ttu-id="6f050-103">Aktualisiert eine dem Anwendungsgateway zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="6f050-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="6f050-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f050-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f050-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f050-105">DESCRIPTION</span></span>
<span data-ttu-id="6f050-106">Das **Cmdlet "Set-AzApplicationGatewayIdentity"** aktualisiert eine Dem Anwendungsgateway zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="6f050-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="6f050-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f050-107">EXAMPLES</span></span>

### <span data-ttu-id="6f050-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f050-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="6f050-109">In diesem Beispiel weisen wir einem vorhandenen Anwendungsgateway eine Benutzeridentität zu.</span><span class="sxs-lookup"><span data-stu-id="6f050-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="6f050-110">Hinweis: Diese Identität sollte Zugriff auf das Keyvault haben, aus dem auf die Zertifikate/Geheimschlüssel verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6f050-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="6f050-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f050-111">PARAMETERS</span></span>

### <span data-ttu-id="6f050-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f050-112">-ApplicationGateway</span></span>
<span data-ttu-id="6f050-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f050-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f050-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f050-114">-DefaultProfile</span></span>
<span data-ttu-id="6f050-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f050-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f050-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="6f050-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="6f050-117">ResourceId der dem Anwendungsgateway zugewiesenen Benutzeridentität.</span><span class="sxs-lookup"><span data-stu-id="6f050-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f050-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f050-118">-Confirm</span></span>
<span data-ttu-id="6f050-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f050-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f050-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6f050-120">-WhatIf</span></span>
<span data-ttu-id="6f050-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f050-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f050-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f050-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f050-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f050-123">CommonParameters</span></span>
<span data-ttu-id="6f050-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f050-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f050-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f050-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f050-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f050-126">INPUTS</span></span>

### <span data-ttu-id="6f050-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f050-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="6f050-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6f050-128">System.String</span></span>

## <span data-ttu-id="6f050-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f050-129">OUTPUTS</span></span>

### <span data-ttu-id="6f050-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f050-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f050-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f050-131">NOTES</span></span>

## <span data-ttu-id="6f050-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f050-132">RELATED LINKS</span></span>
