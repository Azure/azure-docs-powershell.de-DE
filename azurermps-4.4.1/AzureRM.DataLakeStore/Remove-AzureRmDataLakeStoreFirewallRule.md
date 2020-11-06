---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 6bbdfa981ac1d9e80c377bf2835cff73c99a7a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500857"
---
# <span data-ttu-id="df3a3-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="df3a3-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="df3a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df3a3-102">SYNOPSIS</span></span>
<span data-ttu-id="df3a3-103">Entfernt die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="df3a3-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df3a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df3a3-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df3a3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df3a3-105">DESCRIPTION</span></span>
<span data-ttu-id="df3a3-106">Das Cmdlet **Remove-AzureRmDataLakeStoreFirewallRule** entfernt die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="df3a3-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="df3a3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df3a3-107">EXAMPLES</span></span>

### <span data-ttu-id="df3a3-108">Beispiel 1: Entfernen einer Firewall-Regel von einem Konto</span><span class="sxs-lookup"><span data-stu-id="df3a3-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="df3a3-109">Entfernt die Firewall-Regel "MyFirewallRule" aus dem Konto "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="df3a3-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="df3a3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="df3a3-110">PARAMETERS</span></span>

### <span data-ttu-id="df3a3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="df3a3-111">-Account</span></span>
<span data-ttu-id="df3a3-112">Das Data Lake Store-Konto zum Aktualisieren der Firewall-Regel in</span><span class="sxs-lookup"><span data-stu-id="df3a3-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="df3a3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="df3a3-113">-Name</span></span>
<span data-ttu-id="df3a3-114">Der Name der Firewall-Regel, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="df3a3-114">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="df3a3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df3a3-115">-PassThru</span></span>
<span data-ttu-id="df3a3-116">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="df3a3-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df3a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df3a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="df3a3-118">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, aus dem die Firewall-Regel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="df3a3-118">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df3a3-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df3a3-119">-Confirm</span></span>
<span data-ttu-id="df3a3-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df3a3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df3a3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df3a3-121">-WhatIf</span></span>
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

### <span data-ttu-id="df3a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df3a3-122">-DefaultProfile</span></span>
<span data-ttu-id="df3a3-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df3a3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df3a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df3a3-124">CommonParameters</span></span>
<span data-ttu-id="df3a3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df3a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df3a3-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df3a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df3a3-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df3a3-127">INPUTS</span></span>

## <span data-ttu-id="df3a3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df3a3-128">OUTPUTS</span></span>

### <span data-ttu-id="df3a3-129">bool</span><span class="sxs-lookup"><span data-stu-id="df3a3-129">bool</span></span>
<span data-ttu-id="df3a3-130">Wenn passthru angegeben ist, wird nach dem erfolgreichen Abschluss "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df3a3-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="df3a3-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="df3a3-131">NOTES</span></span>

## <span data-ttu-id="df3a3-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df3a3-132">RELATED LINKS</span></span>

