---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
ms.openlocfilehash: 167678bfe84117cdc53e9e90b520abe24fed4b92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165948"
---
# <span data-ttu-id="c392d-101">New-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="c392d-101">New-AzSubscription</span></span>

## <span data-ttu-id="c392d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c392d-102">SYNOPSIS</span></span>
<span data-ttu-id="c392d-103">Erstellt ein Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c392d-103">Creates an Azure subscription.</span></span>

## <span data-ttu-id="c392d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c392d-104">SYNTAX</span></span>

```
New-AzSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c392d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c392d-105">DESCRIPTION</span></span>
<span data-ttu-id="c392d-106">Das Cmdlet **New-AzSubscription** erstellt ein Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c392d-106">The **New-AzSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="c392d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c392d-107">EXAMPLES</span></span>

### <span data-ttu-id="c392d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c392d-108">Example 1</span></span>
```
PS C:\> New-AzSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="c392d-109">Erstellt ein Azure-Abonnement unter dem angegebenen registrierungskonto mit dem angegebenen Angebotstyp.</span><span class="sxs-lookup"><span data-stu-id="c392d-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="c392d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c392d-110">PARAMETERS</span></span>

### <span data-ttu-id="c392d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c392d-111">-AsJob</span></span>
<span data-ttu-id="c392d-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c392d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c392d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c392d-113">-DefaultProfile</span></span>
<span data-ttu-id="c392d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c392d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c392d-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="c392d-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="c392d-116">Der Name des für die Erstellung des Abonnements zu verwendenden Registrierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="c392d-116">Name of the enrollment account to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c392d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c392d-117">-Name</span></span>
<span data-ttu-id="c392d-118">Der Name des zu erstellendes Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c392d-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c392d-119">-Angebottype</span><span class="sxs-lookup"><span data-stu-id="c392d-119">-OfferType</span></span>
<span data-ttu-id="c392d-120">Der Typ des Angebots, das beim Erstellen des Abonnements verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c392d-120">The type of offer to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c392d-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="c392d-121">-OwnerApplicationId</span></span>
<span data-ttu-id="c392d-122">Der APP-SPN (s), dem Besitzer Zugriff auf das Abonnement gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c392d-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c392d-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="c392d-123">-OwnerObjectId</span></span>
<span data-ttu-id="c392d-124">Die Benutzer-oder Gruppen-IDs (n), denen der Besitzer Zugriff auf das Abonnement gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c392d-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c392d-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="c392d-125">-OwnerSignInName</span></span>
<span data-ttu-id="c392d-126">Die Benutzer, denen der Besitzer Zugriff auf das Abonnement gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c392d-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c392d-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c392d-127">-Confirm</span></span>
<span data-ttu-id="c392d-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c392d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c392d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c392d-129">-WhatIf</span></span>
<span data-ttu-id="c392d-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c392d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c392d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c392d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c392d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c392d-132">CommonParameters</span></span>
<span data-ttu-id="c392d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c392d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c392d-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c392d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c392d-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c392d-135">INPUTS</span></span>

### <span data-ttu-id="c392d-136">Keine</span><span class="sxs-lookup"><span data-stu-id="c392d-136">None</span></span>

## <span data-ttu-id="c392d-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c392d-137">OUTPUTS</span></span>

### <span data-ttu-id="c392d-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="c392d-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="c392d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c392d-139">NOTES</span></span>

## <span data-ttu-id="c392d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c392d-140">RELATED LINKS</span></span>
