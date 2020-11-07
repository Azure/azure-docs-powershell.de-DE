---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 83a44e97e01e846cec568227514177babd76d30a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660255"
---
# <span data-ttu-id="4ef99-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="4ef99-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="4ef99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ef99-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef99-103">Aktualisiert eine dem Anwendungsgateway zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="4ef99-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="4ef99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ef99-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ef99-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ef99-105">DESCRIPTION</span></span>
<span data-ttu-id="4ef99-106">Das Cmdlet " **Satz-AzApplicationGatewayIdentity** " aktualisiert eine dem Application Gateway zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="4ef99-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="4ef99-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ef99-107">EXAMPLES</span></span>

### <span data-ttu-id="4ef99-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ef99-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="4ef99-109">In diesem Beispiel weisen wir einem vorhandenen Application Gateway eine Benutzer zugewiesene Identität zu.</span><span class="sxs-lookup"><span data-stu-id="4ef99-109">In this example, we assign a user assigned identity to an existing applicaiton gateway.</span></span>
<span data-ttu-id="4ef99-110">Hinweis: Diese Identität sollte auf das keyvault zugreifen können, aus dem die Zertifikate/Geheimnisse referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="4ef99-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="4ef99-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ef99-111">PARAMETERS</span></span>

### <span data-ttu-id="4ef99-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ef99-112">-ApplicationGateway</span></span>
<span data-ttu-id="4ef99-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ef99-113">The applicationGateway</span></span>

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

### <span data-ttu-id="4ef99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef99-114">-DefaultProfile</span></span>
<span data-ttu-id="4ef99-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ef99-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ef99-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="4ef99-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="4ef99-117">Die ID des Benutzers, der dem Application Gateway zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ef99-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="4ef99-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ef99-118">-Confirm</span></span>
<span data-ttu-id="4ef99-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ef99-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ef99-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef99-120">-WhatIf</span></span>
<span data-ttu-id="4ef99-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ef99-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ef99-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ef99-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ef99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef99-123">CommonParameters</span></span>
<span data-ttu-id="4ef99-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef99-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef99-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef99-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ef99-126">INPUTS</span></span>

### <span data-ttu-id="4ef99-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ef99-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="4ef99-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ef99-128">System.String</span></span>

## <span data-ttu-id="4ef99-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ef99-129">OUTPUTS</span></span>

### <span data-ttu-id="4ef99-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ef99-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ef99-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ef99-131">NOTES</span></span>

## <span data-ttu-id="4ef99-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ef99-132">RELATED LINKS</span></span>
