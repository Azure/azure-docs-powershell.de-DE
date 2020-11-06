---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/invoke-azurermservermanagementpowershellcommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: d4720a1159d55064a007a97df7233853200f1295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480922"
---
# <span data-ttu-id="1427f-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="1427f-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="1427f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1427f-102">SYNOPSIS</span></span>
<span data-ttu-id="1427f-103">Führt einen Windows PowerShell-Skriptblock auf einem Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="1427f-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1427f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1427f-104">SYNTAX</span></span>

### <span data-ttu-id="1427f-105">ByName</span><span class="sxs-lookup"><span data-stu-id="1427f-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1427f-106">BySession</span><span class="sxs-lookup"><span data-stu-id="1427f-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1427f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1427f-107">DESCRIPTION</span></span>
<span data-ttu-id="1427f-108">Das Cmdlet **Invoke-AzureRmServerManagementPowerShellCommand** führt einen Windows PowerShell-Skriptblock auf einem Knoten aus, der von einem Azure Server-Verwaltungs Gateway verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="1427f-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="1427f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1427f-109">EXAMPLES</span></span>

## <span data-ttu-id="1427f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1427f-110">PARAMETERS</span></span>

### <span data-ttu-id="1427f-111">-Befehl</span><span class="sxs-lookup"><span data-stu-id="1427f-111">-Command</span></span>
<span data-ttu-id="1427f-112">Gibt den Skriptblock an, der auf dem Zielknoten ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1427f-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1427f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1427f-113">-DefaultProfile</span></span>
<span data-ttu-id="1427f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1427f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1427f-115">-Nodename</span><span class="sxs-lookup"><span data-stu-id="1427f-115">-NodeName</span></span>
<span data-ttu-id="1427f-116">Gibt den Namen des Knotens an, auf dem der Skriptblock ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1427f-116">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1427f-117">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="1427f-117">-PowerShellSessionName</span></span>
<span data-ttu-id="1427f-118">Gibt den Namen des Windows PowerShell-Speicherplatzes auf dem Zielknoten an.</span><span class="sxs-lookup"><span data-stu-id="1427f-118">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1427f-119">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="1427f-119">-RawOutput</span></span>
<span data-ttu-id="1427f-120">Gibt an, dass das Cmdlet das vollständige Objekt zurückgibt, das die Ausgabe des Knotens enthält.</span><span class="sxs-lookup"><span data-stu-id="1427f-120">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1427f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1427f-121">-ResourceGroupName</span></span>
<span data-ttu-id="1427f-122">Gibt den Namen der Ressourcengruppe an, zu der der Knoten gehört.</span><span class="sxs-lookup"><span data-stu-id="1427f-122">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1427f-123">-Sitzung</span><span class="sxs-lookup"><span data-stu-id="1427f-123">-Session</span></span>
<span data-ttu-id="1427f-124">Gibt das **Sitzungs** Objekt an, das dieses Cmdlet zum Herstellen einer Verbindung mit dem Zielknoten verwendet.</span><span class="sxs-lookup"><span data-stu-id="1427f-124">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="1427f-125">Dieser Parameter kann anstelle der *ResourceGroupName* -, *NodeName* -, *Sessionname* -und *PowerShellSessionName* -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1427f-125">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1427f-126">-Sitzungsname</span><span class="sxs-lookup"><span data-stu-id="1427f-126">-SessionName</span></span>
<span data-ttu-id="1427f-127">Gibt den Namen der Sitzung an, in der der Knoten verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1427f-127">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1427f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1427f-128">CommonParameters</span></span>
<span data-ttu-id="1427f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1427f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1427f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1427f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1427f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1427f-131">INPUTS</span></span>

### <span data-ttu-id="1427f-132">Sitzung</span><span class="sxs-lookup"><span data-stu-id="1427f-132">Session</span></span>
<span data-ttu-id="1427f-133">Der Parameter "Session" akzeptiert den Wert vom Typ "Session" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1427f-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="1427f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1427f-134">OUTPUTS</span></span>

### <span data-ttu-id="1427f-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="1427f-135">System.Object</span></span>

## <span data-ttu-id="1427f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="1427f-136">NOTES</span></span>

## <span data-ttu-id="1427f-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1427f-137">RELATED LINKS</span></span>

[<span data-ttu-id="1427f-138">Azure Server-Verwaltungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1427f-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


