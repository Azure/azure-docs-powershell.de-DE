---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305691"
---
# <span data-ttu-id="570c4-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="570c4-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="570c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="570c4-102">SYNOPSIS</span></span>
<span data-ttu-id="570c4-103">Erstellt ein Identitätsobjekt für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="570c4-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="570c4-104">Dadurch wird auf die vom Benutzer zugewiesene Identität verwiesen.</span><span class="sxs-lookup"><span data-stu-id="570c4-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="570c4-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="570c4-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="570c4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="570c4-106">DESCRIPTION</span></span>
<span data-ttu-id="570c4-107">**Das Cmdlet "New-AzApplicationGatewayIdentity"** erstellt ein Anwendungsgateway-Identitätsobjekt.</span><span class="sxs-lookup"><span data-stu-id="570c4-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="570c4-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="570c4-108">EXAMPLES</span></span>

### <span data-ttu-id="570c4-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="570c4-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="570c4-110">In diesem Beispiel erstellen wir eine vom Benutzer zugewiesene Identität und verweisen dann in einem Identitätsobjekt darauf, das mit dem Anwendungsgateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="570c4-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="570c4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="570c4-111">PARAMETERS</span></span>

### <span data-ttu-id="570c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="570c4-112">-DefaultProfile</span></span>
<span data-ttu-id="570c4-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="570c4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="570c4-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="570c4-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="570c4-115">ResourceId der dem Anwendungsgateway zugewiesenen Benutzeridentität.</span><span class="sxs-lookup"><span data-stu-id="570c4-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="570c4-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="570c4-116">-Confirm</span></span>
<span data-ttu-id="570c4-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="570c4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="570c4-118">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="570c4-118">-WhatIf</span></span>
<span data-ttu-id="570c4-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="570c4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="570c4-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="570c4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="570c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="570c4-121">CommonParameters</span></span>
<span data-ttu-id="570c4-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="570c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="570c4-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="570c4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="570c4-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="570c4-124">INPUTS</span></span>

### <span data-ttu-id="570c4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="570c4-125">System.String</span></span>

## <span data-ttu-id="570c4-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="570c4-126">OUTPUTS</span></span>

### <span data-ttu-id="570c4-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="570c4-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="570c4-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="570c4-128">NOTES</span></span>

## <span data-ttu-id="570c4-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="570c4-129">RELATED LINKS</span></span>
