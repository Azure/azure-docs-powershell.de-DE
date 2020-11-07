---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 3bb2df6349c734e9802183c13eb39ae8ceafc50b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821644"
---
# <span data-ttu-id="f7731-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="f7731-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="f7731-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7731-102">SYNOPSIS</span></span>
<span data-ttu-id="f7731-103">Erstellt ein Identity-Objekt für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f7731-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="f7731-104">Hierbei handelt es sich um einen Verweis auf die Benutzer zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="f7731-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="f7731-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7731-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7731-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7731-106">DESCRIPTION</span></span>
<span data-ttu-id="f7731-107">**New-AzApplicationGatewayIdentity-** Cmdlet erstellt ein Identity-Objekt für ein Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f7731-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="f7731-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7731-108">EXAMPLES</span></span>

### <span data-ttu-id="f7731-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7731-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="f7731-110">In diesem Beispiel erstellen wir eine Benutzer zugewiesene Identität und verweisen dann im mit Application Gateway verwendeten Identity-Objekt darauf.</span><span class="sxs-lookup"><span data-stu-id="f7731-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="f7731-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7731-111">PARAMETERS</span></span>

### <span data-ttu-id="f7731-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7731-112">-DefaultProfile</span></span>
<span data-ttu-id="f7731-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7731-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7731-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f7731-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f7731-115">Die ID des Benutzers, der dem Application Gateway zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7731-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="f7731-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7731-116">-Confirm</span></span>
<span data-ttu-id="f7731-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7731-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7731-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7731-118">-WhatIf</span></span>
<span data-ttu-id="f7731-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7731-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7731-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7731-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7731-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7731-121">CommonParameters</span></span>
<span data-ttu-id="f7731-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7731-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7731-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7731-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7731-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7731-124">INPUTS</span></span>

### <span data-ttu-id="f7731-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f7731-125">System.String</span></span>

## <span data-ttu-id="f7731-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7731-126">OUTPUTS</span></span>

### <span data-ttu-id="f7731-127">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f7731-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="f7731-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7731-128">NOTES</span></span>

## <span data-ttu-id="f7731-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7731-129">RELATED LINKS</span></span>
