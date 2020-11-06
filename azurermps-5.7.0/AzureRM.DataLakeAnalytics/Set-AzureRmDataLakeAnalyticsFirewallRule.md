---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 98ebcd2380cf20d9fbe12d9538f112c8efca5335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482994"
---
# <span data-ttu-id="056b6-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="056b6-101">Set-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="056b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="056b6-102">SYNOPSIS</span></span>
<span data-ttu-id="056b6-103">Aktualisiert eine Firewall-Regel in einem Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="056b6-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="056b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="056b6-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="056b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="056b6-105">DESCRIPTION</span></span>
<span data-ttu-id="056b6-106">Das Cmdlet " **Satz-AzureRmDataLakeAnalyticsFirewallRule** " aktualisiert eine Firewallregel in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="056b6-106">The **Set-AzureRmDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="056b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="056b6-107">EXAMPLES</span></span>

### <span data-ttu-id="056b6-108">Beispiel 1: Aktualisieren einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="056b6-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="056b6-109">Dieser Befehl aktualisiert die Firewallregel mit dem Namen "meine Firewall-Regel" im Konto "ContosoAdlAcct", um den neuen IP-Bereich zu haben: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="056b6-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="056b6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="056b6-110">PARAMETERS</span></span>

### <span data-ttu-id="056b6-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="056b6-111">-Account</span></span>
<span data-ttu-id="056b6-112">Das Data Lake Analytics-Konto zum Aktualisieren der Firewall-Regel in</span><span class="sxs-lookup"><span data-stu-id="056b6-112">The Data Lake Analytics account to update the firewall rule in</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="056b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="056b6-113">-DefaultProfile</span></span>
<span data-ttu-id="056b6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="056b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="056b6-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="056b6-115">-EndIpAddress</span></span>
<span data-ttu-id="056b6-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="056b6-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="056b6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="056b6-117">-Name</span></span>
<span data-ttu-id="056b6-118">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="056b6-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="056b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="056b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="056b6-120">Der Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="056b6-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="056b6-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="056b6-121">-StartIpAddress</span></span>
<span data-ttu-id="056b6-122">Der Anfang des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="056b6-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="056b6-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="056b6-123">-Confirm</span></span>
<span data-ttu-id="056b6-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="056b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="056b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="056b6-125">-WhatIf</span></span>
<span data-ttu-id="056b6-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="056b6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="056b6-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="056b6-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="056b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="056b6-128">CommonParameters</span></span>
<span data-ttu-id="056b6-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="056b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="056b6-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="056b6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="056b6-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="056b6-131">INPUTS</span></span>

### <span data-ttu-id="056b6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="056b6-132">System.String</span></span>

## <span data-ttu-id="056b6-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="056b6-133">OUTPUTS</span></span>

### <span data-ttu-id="056b6-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="056b6-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="056b6-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="056b6-135">NOTES</span></span>

## <span data-ttu-id="056b6-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="056b6-136">RELATED LINKS</span></span>

