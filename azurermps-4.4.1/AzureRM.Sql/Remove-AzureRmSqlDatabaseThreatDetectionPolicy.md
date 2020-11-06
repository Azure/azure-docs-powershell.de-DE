---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 723e765435aae739e6d58320276f7df8ac06ba66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505586"
---
# <span data-ttu-id="aec9f-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aec9f-101">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="aec9f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aec9f-102">SYNOPSIS</span></span>
<span data-ttu-id="aec9f-103">Entfernt die Bedrohungs Erkennungsrichtlinie aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="aec9f-103">Removes the threat detection policy from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aec9f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aec9f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aec9f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aec9f-105">DESCRIPTION</span></span>
<span data-ttu-id="aec9f-106">Das Cmdlet **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** entfernt die Bedrohungs Erkennungsrichtlinie aus einer AzureAzure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="aec9f-106">The **Remove-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="aec9f-107">Um dieses Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -und *Servername* -Parameter an, um die Datenbank zu identifizieren, aus der dieses Cmdlet die Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="aec9f-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="aec9f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aec9f-108">EXAMPLES</span></span>

### <span data-ttu-id="aec9f-109">Beispiel 1: Entfernen einer Bedrohungs Erkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="aec9f-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="aec9f-110">Dieser Befehl entfernt die Richtlinie für die Bedrohungserkennung aus einer Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01.</span><span class="sxs-lookup"><span data-stu-id="aec9f-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="aec9f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="aec9f-111">PARAMETERS</span></span>

### <span data-ttu-id="aec9f-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aec9f-112">-DatabaseName</span></span>
<span data-ttu-id="aec9f-113">Gibt den Namen einer Datenbank an, in der die Bedrohungs Erkennungsrichtlinie entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aec9f-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec9f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aec9f-114">-PassThru</span></span>
<span data-ttu-id="aec9f-115">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="aec9f-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aec9f-116">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="aec9f-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aec9f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec9f-117">-ResourceGroupName</span></span>
<span data-ttu-id="aec9f-118">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="aec9f-118">Specifies the name of the resource group the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec9f-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="aec9f-119">-ServerName</span></span>
<span data-ttu-id="aec9f-120">Gibt den Namen eines Servers an, auf dem die Datenbank ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aec9f-120">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="aec9f-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aec9f-121">-Confirm</span></span>
<span data-ttu-id="aec9f-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aec9f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec9f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec9f-123">-WhatIf</span></span>
<span data-ttu-id="aec9f-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aec9f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aec9f-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aec9f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec9f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec9f-126">-DefaultProfile</span></span>
<span data-ttu-id="aec9f-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aec9f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aec9f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec9f-128">CommonParameters</span></span>
<span data-ttu-id="aec9f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec9f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec9f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec9f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec9f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aec9f-131">INPUTS</span></span>

###  
<span data-ttu-id="aec9f-132">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="aec9f-132">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="aec9f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aec9f-133">OUTPUTS</span></span>

### <span data-ttu-id="aec9f-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="aec9f-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="aec9f-135">Dieses Cmdlet gibt ein **DatabaseThreatDetectionPolicyModel** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="aec9f-135">This cmdlet returns a **DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="aec9f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="aec9f-136">NOTES</span></span>

## <span data-ttu-id="aec9f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aec9f-137">RELATED LINKS</span></span>

[<span data-ttu-id="aec9f-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="aec9f-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


