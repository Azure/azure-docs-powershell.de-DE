---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 99acce24389a02c8fb50f5b313841319f813feaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505078"
---
# <span data-ttu-id="2b537-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2b537-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="2b537-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b537-102">SYNOPSIS</span></span>
<span data-ttu-id="2b537-103">Ruft eine Firewall-Regel oder eine Liste mit Firewallregeln aus einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="2b537-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b537-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b537-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b537-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b537-105">DESCRIPTION</span></span>
<span data-ttu-id="2b537-106">Das Cmdlet " **Get-AzureRmDataLakeAnalyticsFirewallRule** " Ruft eine Firewall-Regel oder eine Liste mit Firewallregeln aus einem Azure Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="2b537-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2b537-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b537-107">EXAMPLES</span></span>

### <span data-ttu-id="2b537-108">Beispiel 1: Abrufen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="2b537-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="2b537-109">Dieser Befehl ruft die Firewall-Regel mit dem Namen "meine Firewall-Regel" aus dem Konto "ContosoAdlAcct" ab.</span><span class="sxs-lookup"><span data-stu-id="2b537-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="2b537-110">Beispiel 2: Auflisten aller Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="2b537-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="2b537-111">Dieser Befehl ruft alle Firewallregeln vom Konto "ContosoAdlAcct" ab.</span><span class="sxs-lookup"><span data-stu-id="2b537-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="2b537-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b537-112">PARAMETERS</span></span>

### <span data-ttu-id="2b537-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="2b537-113">-Account</span></span>
<span data-ttu-id="2b537-114">Das Data Lake Analytics-Konto, aus dem die Firewall-Regel abgerufen werden soll</span><span class="sxs-lookup"><span data-stu-id="2b537-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b537-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2b537-115">-Name</span></span>
<span data-ttu-id="2b537-116">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="2b537-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b537-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b537-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b537-118">Der Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b537-118">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b537-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b537-119">-DefaultProfile</span></span>
<span data-ttu-id="2b537-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b537-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b537-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b537-121">CommonParameters</span></span>
<span data-ttu-id="2b537-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b537-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b537-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b537-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b537-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b537-124">INPUTS</span></span>

### <span data-ttu-id="2b537-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2b537-125">System.String</span></span>

## <span data-ttu-id="2b537-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b537-126">OUTPUTS</span></span>

### <span data-ttu-id="2b537-127">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2b537-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>
<span data-ttu-id="2b537-128">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule, Microsoft. Azure. Commands. DataLakeAnalytics, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2b537-128">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule, Microsoft.Azure.Commands.DataLakeAnalytics, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b537-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b537-129">NOTES</span></span>

## <span data-ttu-id="2b537-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b537-130">RELATED LINKS</span></span>

