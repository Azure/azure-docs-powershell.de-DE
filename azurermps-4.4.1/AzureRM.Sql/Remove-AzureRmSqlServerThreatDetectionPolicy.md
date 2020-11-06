---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479845"
---
# <span data-ttu-id="affe2-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="affe2-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="affe2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="affe2-102">SYNOPSIS</span></span>
<span data-ttu-id="affe2-103">Entfernt die Bedrohungs Erkennungsrichtlinie von einem Server.</span><span class="sxs-lookup"><span data-stu-id="affe2-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="affe2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="affe2-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="affe2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="affe2-105">DESCRIPTION</span></span>
<span data-ttu-id="affe2-106">Das Remove-AzureRmSqlServerThreatDetectionPolicy-Cmdlet entfernt die Richtlinie für die Bedrohungserkennung aus einem Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="affe2-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="affe2-107">Um dieses Cmdlet zu verwenden, geben Sie die ResourceGroupName-und Servername-Parameter an, um den Server zu identifizieren, auf dem dieses Cmdlet die Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="affe2-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="affe2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="affe2-108">EXAMPLES</span></span>

### <span data-ttu-id="affe2-109">--------------------------Beispiel 1: Entfernen einer Bedrohungs Erkennungsrichtlinie für eine Datenbank--------------------------</span><span class="sxs-lookup"><span data-stu-id="affe2-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="affe2-110">Mit diesem Befehl wird die Bedrohungs Erkennungsrichtlinie von einem Server namens "Server01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="affe2-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="affe2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="affe2-111">PARAMETERS</span></span>

### <span data-ttu-id="affe2-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="affe2-112">-PassThru</span></span>
<span data-ttu-id="affe2-113">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="affe2-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="affe2-114">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="affe2-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="affe2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="affe2-115">-ResourceGroupName</span></span>
<span data-ttu-id="affe2-116">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="affe2-116">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="affe2-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="affe2-117">-ServerName</span></span>
<span data-ttu-id="affe2-118">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="affe2-118">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affe2-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="affe2-119">-Confirm</span></span>
<span data-ttu-id="affe2-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="affe2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="affe2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="affe2-121">-WhatIf</span></span>
<span data-ttu-id="affe2-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="affe2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="affe2-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="affe2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="affe2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affe2-124">-DefaultProfile</span></span>
<span data-ttu-id="affe2-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="affe2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="affe2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affe2-126">CommonParameters</span></span>
<span data-ttu-id="affe2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="affe2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affe2-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="affe2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affe2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="affe2-129">INPUTS</span></span>

###  
<span data-ttu-id="affe2-130">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="affe2-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="affe2-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="affe2-131">OUTPUTS</span></span>

### <span data-ttu-id="affe2-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="affe2-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="affe2-133">Dieses Cmdlet gibt ein ServerThreatDetectionPolicyModel-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="affe2-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="affe2-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="affe2-134">NOTES</span></span>

## <span data-ttu-id="affe2-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="affe2-135">RELATED LINKS</span></span>

[<span data-ttu-id="affe2-136">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="affe2-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

