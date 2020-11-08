---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176346"
---
# <span data-ttu-id="47685-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="47685-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="47685-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47685-102">SYNOPSIS</span></span>
<span data-ttu-id="47685-103">Listet die Zugriffstaste für den angegebenen Konfigurationsspeicher auf.</span><span class="sxs-lookup"><span data-stu-id="47685-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="47685-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47685-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47685-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47685-105">DESCRIPTION</span></span>
<span data-ttu-id="47685-106">Listet die Zugriffstaste für den angegebenen Konfigurationsspeicher auf.</span><span class="sxs-lookup"><span data-stu-id="47685-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="47685-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47685-107">EXAMPLES</span></span>

### <span data-ttu-id="47685-108">Beispiel 1: Auflisten aller Store-Schlüssel eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="47685-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="47685-109">Dieser Befehl listet alle Store-Schlüssel eines App-Konfigurationsspeichers auf.</span><span class="sxs-lookup"><span data-stu-id="47685-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="47685-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="47685-110">PARAMETERS</span></span>

### <span data-ttu-id="47685-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47685-111">-DefaultProfile</span></span>
<span data-ttu-id="47685-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47685-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47685-113">-Name</span><span class="sxs-lookup"><span data-stu-id="47685-113">-Name</span></span>
<span data-ttu-id="47685-114">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="47685-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="47685-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47685-115">-ResourceGroupName</span></span>
<span data-ttu-id="47685-116">Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="47685-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="47685-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="47685-117">-SubscriptionId</span></span>
<span data-ttu-id="47685-118">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="47685-118">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="47685-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47685-119">-Confirm</span></span>
<span data-ttu-id="47685-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47685-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47685-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47685-121">-WhatIf</span></span>
<span data-ttu-id="47685-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47685-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47685-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47685-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47685-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47685-124">CommonParameters</span></span>
<span data-ttu-id="47685-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47685-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47685-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47685-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47685-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47685-127">INPUTS</span></span>

## <span data-ttu-id="47685-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47685-128">OUTPUTS</span></span>

### <span data-ttu-id="47685-129">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. IApiKey</span><span class="sxs-lookup"><span data-stu-id="47685-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="47685-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="47685-130">NOTES</span></span>

<span data-ttu-id="47685-131">Aliase</span><span class="sxs-lookup"><span data-stu-id="47685-131">ALIASES</span></span>

## <span data-ttu-id="47685-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47685-132">RELATED LINKS</span></span>

