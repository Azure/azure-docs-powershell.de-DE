---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: 82e5f6ced22b17c8966afbd5bc57324ab2069d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938960"
---
# <span data-ttu-id="77752-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="77752-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="77752-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77752-102">SYNOPSIS</span></span>
<span data-ttu-id="77752-103">Holen Sie sich die Zugriffstasten der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="77752-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="77752-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77752-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="77752-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77752-105">DESCRIPTION</span></span>
<span data-ttu-id="77752-106">Holen Sie sich die Zugriffstasten der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="77752-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="77752-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="77752-107">EXAMPLES</span></span>

### <span data-ttu-id="77752-108">Beispiel 1: Abrufen des Schlüssels für den angegebenen Kommunikationsdienst</span><span class="sxs-lookup"><span data-stu-id="77752-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="77752-109">Zeigt die Verbindungszeichenfolge und den Schlüssel für den angegebenen Kommunikationsdienst an.</span><span class="sxs-lookup"><span data-stu-id="77752-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="77752-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="77752-110">PARAMETERS</span></span>

### <span data-ttu-id="77752-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="77752-111">-CommunicationServiceName</span></span>
<span data-ttu-id="77752-112">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="77752-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="77752-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77752-113">-DefaultProfile</span></span>
<span data-ttu-id="77752-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77752-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77752-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77752-115">-ResourceGroupName</span></span>
<span data-ttu-id="77752-116">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="77752-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="77752-117">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="77752-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="77752-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77752-118">-SubscriptionId</span></span>
<span data-ttu-id="77752-119">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="77752-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="77752-120">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="77752-120">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77752-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77752-121">-Confirm</span></span>
<span data-ttu-id="77752-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77752-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77752-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77752-123">-WhatIf</span></span>
<span data-ttu-id="77752-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77752-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77752-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77752-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77752-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77752-126">CommonParameters</span></span>
<span data-ttu-id="77752-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77752-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77752-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77752-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77752-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="77752-129">INPUTS</span></span>

## <span data-ttu-id="77752-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="77752-130">OUTPUTS</span></span>

### <span data-ttu-id="77752-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="77752-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="77752-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="77752-132">NOTES</span></span>

<span data-ttu-id="77752-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="77752-133">ALIASES</span></span>

## <span data-ttu-id="77752-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="77752-134">RELATED LINKS</span></span>

