---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 3ad3e98e6fb2ab5c6e0b04495142861ecfe9e0ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498974"
---
# <span data-ttu-id="ba8e4-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ba8e4-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="ba8e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8e4-103">Ändert die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ba8e4-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba8e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba8e4-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba8e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba8e4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8e4-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreFirewallRule** " ändert die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ba8e4-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="ba8e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba8e4-107">EXAMPLES</span></span>

### <span data-ttu-id="ba8e4-108">Beispiel 1: Aktualisieren des Start-und endip-Bereichs für eine Firewallregel</span><span class="sxs-lookup"><span data-stu-id="ba8e4-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="ba8e4-109">Aktualisiert die Firewall-Regel "MyFirewallRule" im Konto "ContosoADL" auf einen Bereich von 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="ba8e4-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="ba8e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba8e4-110">PARAMETERS</span></span>

### <span data-ttu-id="ba8e4-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="ba8e4-111">-Account</span></span>
<span data-ttu-id="ba8e4-112">Das Data Lake Store-Konto zum Aktualisieren der Firewall-Regel in</span><span class="sxs-lookup"><span data-stu-id="ba8e4-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="ba8e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8e4-113">-DefaultProfile</span></span>
<span data-ttu-id="ba8e4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ba8e4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba8e4-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ba8e4-115">-EndIpAddress</span></span>
<span data-ttu-id="ba8e4-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="ba8e4-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="ba8e4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ba8e4-117">-Name</span></span>
<span data-ttu-id="ba8e4-118">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="ba8e4-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="ba8e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba8e4-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das die Firewall-Regel aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba8e4-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="ba8e4-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ba8e4-121">-StartIpAddress</span></span>
<span data-ttu-id="ba8e4-122">Der Anfang des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="ba8e4-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="ba8e4-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba8e4-123">-Confirm</span></span>
<span data-ttu-id="ba8e4-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba8e4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8e4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba8e4-125">-WhatIf</span></span>
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

### <span data-ttu-id="ba8e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8e4-126">CommonParameters</span></span>
<span data-ttu-id="ba8e4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8e4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba8e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8e4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba8e4-129">INPUTS</span></span>

### <span data-ttu-id="ba8e4-130">Keine</span><span class="sxs-lookup"><span data-stu-id="ba8e4-130">None</span></span>
<span data-ttu-id="ba8e4-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ba8e4-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba8e4-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba8e4-132">OUTPUTS</span></span>

### <span data-ttu-id="ba8e4-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ba8e4-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="ba8e4-134">Die Details der aktualisierten Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="ba8e4-134">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="ba8e4-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba8e4-135">NOTES</span></span>

## <span data-ttu-id="ba8e4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba8e4-136">RELATED LINKS</span></span>

