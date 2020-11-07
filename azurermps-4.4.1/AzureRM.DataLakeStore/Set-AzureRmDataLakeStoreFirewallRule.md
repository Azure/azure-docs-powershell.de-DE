---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 30a1599468851da5f01e10dc94af6586d3ecaf8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663586"
---
# <span data-ttu-id="1187e-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1187e-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="1187e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1187e-102">SYNOPSIS</span></span>
<span data-ttu-id="1187e-103">Ändert die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1187e-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1187e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1187e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1187e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1187e-105">DESCRIPTION</span></span>
<span data-ttu-id="1187e-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreFirewallRule** " ändert die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1187e-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1187e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1187e-107">EXAMPLES</span></span>

### <span data-ttu-id="1187e-108">Beispiel 1: Aktualisieren des Start-und endip-Bereichs für eine Firewallregel</span><span class="sxs-lookup"><span data-stu-id="1187e-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="1187e-109">Aktualisiert die Firewall-Regel "MyFirewallRule" im Konto "ContosoADL" auf einen Bereich von 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="1187e-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="1187e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1187e-110">PARAMETERS</span></span>

### <span data-ttu-id="1187e-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1187e-111">-Account</span></span>
<span data-ttu-id="1187e-112">Das Data Lake Store-Konto zum Aktualisieren der Firewall-Regel in</span><span class="sxs-lookup"><span data-stu-id="1187e-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="1187e-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="1187e-113">-EndIpAddress</span></span>
<span data-ttu-id="1187e-114">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="1187e-114">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1187e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1187e-115">-Name</span></span>
<span data-ttu-id="1187e-116">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="1187e-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1187e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1187e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1187e-118">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das die Firewall-Regel aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1187e-118">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1187e-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="1187e-119">-StartIpAddress</span></span>
<span data-ttu-id="1187e-120">Der Anfang des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="1187e-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="1187e-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1187e-121">-Confirm</span></span>
<span data-ttu-id="1187e-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1187e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1187e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1187e-123">-WhatIf</span></span>
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

### <span data-ttu-id="1187e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1187e-124">-DefaultProfile</span></span>
<span data-ttu-id="1187e-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1187e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1187e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1187e-126">CommonParameters</span></span>
<span data-ttu-id="1187e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1187e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1187e-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1187e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1187e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1187e-129">INPUTS</span></span>

## <span data-ttu-id="1187e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1187e-130">OUTPUTS</span></span>

### <span data-ttu-id="1187e-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1187e-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="1187e-132">Die Details der aktualisierten Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="1187e-132">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="1187e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1187e-133">NOTES</span></span>

## <span data-ttu-id="1187e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1187e-134">RELATED LINKS</span></span>

